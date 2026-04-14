---
title: "Signal Infrastructure"
type: concept
tags: [gtm, data, signals, intent, infrastructure, targeting]
created: 2026-04-14
updated: 2026-04-14
sources: [alexvacca-gtm-engineering-hire]
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
| Content engagement | Liked a LinkedIn post, read an article | [[Common Room]] |

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

- [[sources/alexvacca-gtm-engineering-hire]] — primary source
- [[GTM Engineering]] — the practice signal infrastructure enables
- [[Enrichment Waterfall]] — what happens to a lead after the signal fires
- [[Clay]] — where signal data is processed into enriched prospect records
- [[Common Room]], [[Trigify]], [[RB2B]] — signal platforms
- [[Data Warehouse for AI]] — related concept from Schneider's stack
