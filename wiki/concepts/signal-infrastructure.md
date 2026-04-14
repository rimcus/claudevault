---
title: "Signal Infrastructure"
type: concept
tags: [gtm, data, signals, intent, infrastructure, targeting]
created: 2026-04-14
updated: 2026-04-14
sources: [alexvacca-gtm-engineering-hire, salescaptain-linkedin-outbound-playbook]
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

## Relation to "The List is the Strategy"

Signal infrastructure is what makes "the list" actually strategic. A static list is a guess about who might buy. A signal-triggered list is real-time evidence of who is showing buying behavior now.

## See Also

- [[sources/alexvacca-gtm-engineering-hire]] — primary source (intent/firmographic signals)
- [[sources/salescaptain-linkedin-outbound-playbook]] — LinkedIn-specific signal map (7 workflows)
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
