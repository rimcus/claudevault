---
title: "Signal Infrastructure"
type: concept
tags: [gtm, data, signals, intent, infrastructure, targeting]
created: 2026-04-14
updated: 2026-08-11
sources: [alexvacca-gtm-engineering-hire, salescaptain-linkedin-outbound-playbook, codyschneider-andromeda-b2b-facebook, codyschneider-tam-mapping, codyschneider-two-agents-podcast]
---

# Signal Infrastructure

The upstream data layer that tells a GTM system *when* an account is ready to buy — before any email is sent or ad is shown. Includes intent signals, behavioral triggers, and firmographic/technographic changes that indicate purchase readiness. [[Alex Vacca]] identifies this as the layer most companies skip, and skipping it is why campaigns plateau.

## Overview

Most outbound campaigns are built on static lists assembled once and worked through. Signal infrastructure replaces the static list with a **dynamic, continuously-updated feed** of accounts showing real buying intent. Every campaign run on top of signal infrastructure gets smarter over time because the system learns which signals actually convert for a specific ICP.

This is the [[Knowledge Compounding]] principle applied to GTM: the signal layer accumulates learning across campaigns rather than starting from scratch each time.

## Types of Signals

| Signal Type | What It Captures | Example Tools |
|-------------|-----------------|---------------|
| Intent signals | Research behavior on review sites, content consumption | [[Common Room]], [[Trigify]] |
| Hiring triggers | Job postings that indicate a buying moment (e.g. "hiring SDR" = needs sales tools) | |
| Funding events | Recent funding round = budget + growth mode | |
| Technology installs | Installed a competitor or complementary tool | |
| Website visits | Anonymous visitor identification from your own site | [[RB2B]] |
| Content engagement | Liked a LinkedIn post, read an article | [[Common Room]], [[Trigify]] |
| Ad engagement | Engaged with your LinkedIn ad but never clicked | [[Fibbler]] |
| Profile views | Checked your LinkedIn profile before acting | [[Teamfluence]] |
| LinkedIn follows | Followed your company page | LinkedIn export |
| Competitor follows | Follows a competitor's LinkedIn page | LinkedIn + [[Clay]] |

## LinkedIn-Specific Signal Workflows (SalesCaptain)

[[Bill Stathopoulos]] maps 7 concrete signal-triggered workflows for LinkedIn, each with a named signal, motion, and toolchain:

| # | Signal | Trigger | Tools |
|---|--------|---------|-------|
| 01 | Ad Engagers | Engaged with LinkedIn ad, no click | Fibbler/ZenABM → Clay → HeyReach |
| 02 | Content Engagers | 3+ engagements with your posts | Trigify → Clay → HeyReach |
| 03 | Event Attendees | Attended LinkedIn event in your space | Phantombuster → Clay → HeyReach |
| 04 | Keyword Engagers | Posted/commented about your problem space | Trigify → Clay → HeyReach |
| 05 | Page Followers | Followed your LinkedIn company page | LinkedIn export → Clay → Lemlist |
| 06 | Competitor Followers | Follows a competitor | LinkedIn → Clay → HeyReach |
| 07 | Decision Maker | Booked a meeting (pre-warm buying committee) | Calendly → Clay → HeyReach |

**Critical rule:** The signal informs targeting — never the message. Never say "I saw you liked my post." Use the signal to select *who*; use the topic as natural context.

## Why Front-Loading Matters

From Vacca's phase sequence for building a GTM function: signal infrastructure belongs in **Phase 3**, not later. Reason: the system learns which signals convert for *your specific ICP*. Skip it and you're running the old SDR model with fewer people — you'll hit the same ceiling.

## How Signals Flow in the Stack

```
Signal fires (hiring trigger, site visit, intent data)
    → Signal platform (Common Room / Trigify / RB2B)
    → Clay (enrich, qualify, build prospect record)
    → Webhook → routes into correct sequence automatically
    → Instantly / Smartlead (send)
```

The key: the routing happens automatically at signal time. No human has to see the lead before it enters the right campaign.

## The Missing Prerequisite: The TAM Base Map

[[sources/codyschneider-tam-mapping]] (June 2026) identifies the most common signal infrastructure failure mode: signals fire onto unqualified accounts.

> "a signal is noise until it lands on an account you already wanted"

Without a [[TAM Mapping|TAM map]] — a tiered, enriched, named account database — a signal ("company X got funded") has no context. You don't know if the company fits your ICP, what tier it is, or which sequence it should route to. The signal is noise.

**With the TAM map:**
- Signals fire onto accounts you already know you want
- Routing is automatic: "Tier 1 account just got funded → route to Tier 1 sequence"
- No human triage required per signal

**The sequence:** build the map first → layer signals on top. Signal infrastructure deployed without a TAM map is spending on intelligence you can't act on.

## LinkedIn Activity as a Send-List Signal (Abraham, July 2026)

[[sources/nickabraham-linkedin-inmail-pipeline]] extends signal infrastructure into a third context: list hygiene before LinkedIn InMail sends.

[[Nick Abraham]] uses [[Apify]] to filter contact lists for prospects who posted or commented on LinkedIn in the last 30–60 days before loading them into the InMail sequencer. This is a behavioral signal — recent LinkedIn activity predicts message visibility and response rate — applied not to account selection (the TAM layer) but to send-list qualification (the channel layer).

The pattern mirrors the broader signal logic:
- **Account-level signals** (intent data, hiring triggers) tell you *which accounts* to target
- **Contact-level signals** (LinkedIn activity) tell you *which contacts on those accounts* to reach right now
- **Platform-specific signals** (open-profile status) tell you *how* to route each contact within the channel

All three are signal types. The [[LinkedIn InMail Pipeline]] uses all three together.

## LinkedIn Sourcing Mechanics: Feed, Outliers, Engagers (Schneider, August 2026)

[[sources/codyschneider-two-agents-podcast]] adds a fourth context: not filtering an existing list (Abraham, above) or classifying account-level intent (Vacca, TAM), but the mechanics of *building the initial engager list itself* for a cold-outbound agent.

- **Engagement beats firmographics as a hand-raise signal.** LinkedIn reactions/comments outrank firmographic fit as the primary targeting criterion.
- **Track 10–20 category outliers for ~80% coverage.** Rather than tracking every account in a category, a small set of outlier creators/accounts captures most of the category's engagement activity.
- **Source from the For You feed, not search.** LinkedIn's algorithmic feed surfaces what's actually resonating right now; search surfaces stale, generic results.
- **Business accounts work as sources too** — not just individual profiles.
- **The full engager list requires both reactions and comments** — either alone under-counts.
- **A daily cron job** pulls net-new posts from tracked accounts, then extracts engagers from each — the automation cadence that keeps the list current without manual re-pulling.
- **ICP-fit research happens before enrichment, not after.** This ordering rule saves enrichment spend (see [[Enrichment Waterfall]]) on people who wouldn't qualify regardless of contact data quality.

This sits upstream of everything else in this section: it's the mechanism that generates the initial list before any TAM tiering, activity filtering, or signal routing happens to it.

## Signal Infrastructure for Paid Ads: The Andromeda Layer

[[sources/codyschneider-andromeda-b2b-facebook]] extends signal infrastructure into the Facebook ads context. Meta's Andromeda algorithm treats your conversion data as the signal layer — the same "no garbage in, no garbage out" principle that governs GTM agent data warehouses applies to ad platforms:

- **Clean pixel:** correctly fires on real user actions
- **Conversion API (CAPI):** server-side tracking that bypasses browser limitations
- **Real conversion events:** signup and payment — not proxy events like page views

The algorithm learns from these signals to find future converters. Bad signal data corrupts this learning loop the same way bad warehouse data corrupts GTM agent decisions. The "clean data layer" principle applies equally to internal AI agents and external ad platforms.

## Relation to "The List is the Strategy"

Signal infrastructure is what makes "the list" actually strategic. A static list is a guess about who might buy. A signal-triggered list is real-time evidence of who is showing buying behavior now.

## See Also

- [[sources/alexvacca-gtm-engineering-hire]] — primary source (intent/firmographic signals)
- [[sources/salescaptain-linkedin-outbound-playbook]] — LinkedIn-specific signal map (7 workflows)
- [[sources/codyschneider-andromeda-b2b-facebook]] — paid ads signal layer: clean pixel + CAPI + real conversion events
- [[sources/nickabraham-linkedin-inmail-pipeline]] — LinkedIn activity as a contact-level behavioral signal; open-profile status as channel-routing signal
- [[sources/codyschneider-tam-mapping]] — TAM map as prerequisite; signals are noise without a base map
- [[sources/codyschneider-two-agents-podcast]] — LinkedIn engager-list sourcing mechanics: for-you feed, category outliers, business accounts, daily cron
- [[concepts/agent-architecture-principles]] — the design philosophy behind the daily-cron automation described above
- [[TAM Mapping]] — the foundational layer that signals run on top of
- [[concepts/linkedin-inmail-pipeline|LinkedIn InMail Pipeline]] — applies all three signal types (account, contact, platform) in one channel pipeline
- [[GTM Engineering]] — the practice signal infrastructure enables
- [[Content Outbound Flywheel]] — the strategic system these signals feed
- [[Enrichment Waterfall]] — what happens to a lead after the signal fires
- [[Clay]] — where signal data is processed into enriched prospect records
- [[Trigify]] — LinkedIn engagement signal platform
- [[Teamfluence]] — profile viewer tracking
- [[Fibbler]] — LinkedIn ad engager detection
- [[RB2B]] — website visitor deanonymization
- [[Common Room]] — broader intent signal platform
- [[Data Warehouse for AI]] — related concept from Schneider's stack
