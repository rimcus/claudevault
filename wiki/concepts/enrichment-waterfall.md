---
title: "Enrichment Waterfall"
type: concept
tags: [gtm, data, enrichment, targeting, clay]
created: 2026-04-14
updated: 2026-04-14
sources: [alexvacca-gtm-engineering-hire]
---

# Enrichment Waterfall

A multi-provider enrichment strategy in which prospect data is passed sequentially through multiple data providers — each filling gaps the previous one couldn't — until a target data completeness threshold is reached. [[Alex Vacca]] specifies a target of **8–12 data points per prospect** before the first email is drafted.

## Overview

No single enrichment provider has complete coverage for all prospect types. A waterfall stacks providers so if Provider A can't find an email, Provider B tries, then Provider C, and so on. The result is higher coverage than any single provider at a lower per-contact cost than always paying the highest-coverage (most expensive) provider.

In [[Clay]], enrichment waterfalls are a native pattern — you build conditional logic that routes to the next provider based on whether the previous one returned a result.

## Why 8–12 Data Points?

Vacca's specific claim: campaigns built with 8–12 data points per prospect significantly outperform those with 3–5. More data enables:
- More specific targeting criteria (fewer irrelevant prospects make it through)
- More genuinely personalized email openers (specific to their tech stack, team size, recent news)
- Better routing logic (different sequences for different firmographic profiles)

## Common Data Points in the Stack

- Company firmographics (size, revenue, industry, HQ location)
- Technographics (what software they use — indicates budget, workflow, buying patterns)
- Contact email (verified)
- Contact LinkedIn URL
- Recent intent signal (what they've been researching)
- Recent company news (funding, hiring, product launch)
- ICP fit score
- Decision-maker vs. influencer classification

## Providers Mentioned by Vacca

- [[Prospeo]] — enrichment provider
- [[FullEnrich]] — enrichment provider
- [[Apollo]] — also used for enrichment (from Schneider's stack)

## See Also

- [[Signal Infrastructure]] — the upstream layer that feeds the waterfall
- [[GTM Engineering]] — the practice that uses enrichment waterfalls
- [[Clay]] — where waterfalls are built
- [[sources/alexvacca-gtm-engineering-hire]] — source
