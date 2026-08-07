---
title: "Nick Abraham — LinkedIn InMail List Pipeline"
type: source
tags: [linkedin, inmail, outbound, list-building, enrichment, signal, cold-outreach]
created: 2026-07-09
updated: 2026-07-09
sources: [nickabraham-linkedin-inmail-pipeline]
raw: "raw/sources/nickabraham-linkedin-inmail-pipeline.md"
---

# Nick Abraham — LinkedIn InMail List Pipeline

**Source:** X thread by [@NickAbraham12](https://x.com/NickAbraham12/status/2074915461750284796), published 2026-07-08.

**Scale context:** 250,000+ LinkedIn InMails/month, 15+ concurrent campaigns.

## The Core Problem

LinkedIn gives 50 paid InMail credits per [[Sales Navigator]] license per month, plus 400–800 free sends to Open Profiles. If paid credits hit zero, LinkedIn freezes everything — including the free sends. Even 3–5 non-open profiles slipping into the send queue burns the paid balance within a week.

Most teams discover this the hard way: they wake up frozen with no sends going out.

## The 5-Step Pipeline

### Step 1: Pull the Raw List (GetLeads)

Use [[GetLeads]] to build the initial prospect list. For InMail, the only required field is the LinkedIn profile URL — no email, phone, or company domain. The entire system runs from the URL alone.

### Step 2: Enrich for Open-Profile Status (NetNut)

Run every LinkedIn URL through the [[NetNut]] API. It flags which contacts have Open Profile enabled, so you know who can receive free InMails. Split the output into two buckets: open profiles and non-open profiles.

**This segmentation is not optional.** Loading both buckets into a sequencer together is how teams silently drain their paid credit balance.

### Step 3: Filter for Active Users (Apify)

Use [[Apify]] to identify contacts who posted or commented on LinkedIn in the last 30–60 days. Active users are significantly more likely to see and respond to a message. This step lifts response rates across all outbound channels, not just InMail.

### Step 4: Validate ICP Fit (AI Agent)

Run an AI qualification agent across every contact to confirm industry, profile, and role. Total sends are capped, so each one needs to go to a well-qualified prospect. This step enforces credit conservation and quality simultaneously.

### Step 5: Segment Before Loading Into Sequencer

Separate open profiles from non-open before loading any list into the sequencer. Never mix the two buckets in a single sequence.

## Key Statistics

| Metric | Value |
|--------|-------|
| Paid credits per Sales Nav license/month | 50 |
| Free sends to Open Profiles/month | 400–800 |
| Open-profile rate, standard database pull | 5–8% |
| Open-profile rate, Sales Navigator scrape | 30–40% |
| Non-open profiles per day to drain balance in a week | 3–5 |

**Why Sales Navigator has higher open-profile density:** Sales Nav appears to sort open profiles toward the front of search results. A list scraped from Sales Nav naturally skews toward open profiles.

## The Sequencer Trap

Even after running NetNut, open-profile status can change. If a prospect flips their profile to closed between enrichment and send time, and the sequencer doesn't recheck at send, it fires a paid credit on a non-open profile. Sequencer choice matters for InMail — the sequencer must be able to verify open-profile status at send time, not just at list-load time.

## Connection to Existing Concepts

This pipeline is an application of the [[TAM Mapping]] principle: ICP qualification (Step 4) enforces the same machine-sortable fit check before sending that Schneider prescribes before launching any outbound. The active-user filter (Step 3) is a LinkedIn-specific behavioral signal — a variant of [[Signal Infrastructure]] applied to the send list rather than the account universe.

## See Also

- [[entities/nick-abraham|Nick Abraham]] — author; operates at 250K+ InMails/month
- [[concepts/linkedin-inmail-pipeline|LinkedIn InMail Pipeline]] — synthesized concept page for this infrastructure pattern
- [[entities/getleads|GetLeads]] — list building; Step 1
- [[entities/netnut|NetNut]] — open-profile enrichment; Step 2
- [[entities/apify|Apify]] — active user filtering; Step 3
- [[concepts/tam-mapping|TAM Mapping]] — upstream context: ICP definition before list building
- [[concepts/signal-infrastructure|Signal Infrastructure]] — LinkedIn activity as a behavioral signal layer
- [[sources/nickabraham-claude-code-campaign-lists|Nick Abraham — Claude Code Campaign Lists]] — companion source (list management workflow)
