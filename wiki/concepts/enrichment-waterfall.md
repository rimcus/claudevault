---
title: "Enrichment Waterfall"
type: concept
tags: [gtm, data, enrichment, targeting, clay]
created: 2026-04-14
updated: 2026-04-14
sources: [alexvacca-gtm-engineering-hire, salescaptain-linkedin-outbound-playbook, codyschneider-email-generation-agent]
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

## SalesCaptain's Specific Waterfall (Coverage Numbers)

[[Bill Stathopoulos]] gives specific coverage numbers for a 4-step waterfall targeting email addresses:

| Step | Provider | Estimated Coverage |
|------|---------|-------------------|
| 1st pass | [[Findymail]] or Prospeo | ~50–60% |
| 2nd pass | LeadMagic or FullEnrich | fills gaps → ~70–80% [low confidence] |
| 3rd pass | Hunter or [[Apollo]] | final gaps → 85%+ |
| Validation | [[ZeroBounce]] | clean before sending — remove invalid/risky |

**Starting coverage:** ~50% (single-provider baseline)
**After waterfall:** 85%+ — a ~35 percentage-point lift from the cascaded approach.

The validation step is distinct from enrichment: ZeroBounce doesn't find emails, it removes bad ones. Both steps are required for clean deliverability.

## Zero-Cost Alternative: Generate + Verify

[[Cody Schneider]] describes a zero-cost alternative to the paid first-pass: generate every plausible email pattern for a person + domain (given a LinkedIn profile), then existence-check via a cheap API (e.g., mailtester.ninja) and validate with a deliverability tool (MillionVerifier).

**Trade-off vs. paid first-pass:**

| Approach | Cost | Coverage | Limitation |
|----------|------|---------|-----------|
| Paid enrichment (Findymail) | ~$0.01–0.05/contact | ~50–60% | Paid |
| Generate + verify | Near-zero | ~60–70% of non-catch-all domains | Fails on catch-all domains |

**Critical caveat (from @MrColdEmail):** 30–40% of business domains are configured as catch-alls — any email combination returns "valid," making the existence-check step unreliable for those domains. Best suited for SMB campaigns where cost matters and enterprise catch-all domains are less common.

## See Also

- [[Signal Infrastructure]] — the upstream layer that feeds the waterfall
- [[GTM Engineering]] — the practice that uses enrichment waterfalls
- [[Clay]] — where waterfalls are built
- [[Findymail]] — 1st-pass email enrichment provider
- [[ZeroBounce]] — validation layer (final step)
- [[Apollo]] — 3rd-pass enrichment provider
- [[sources/alexvacca-gtm-engineering-hire]] — Vacca's framework (8–12 data points)
- [[sources/salescaptain-linkedin-outbound-playbook]] — SalesCaptain's waterfall with coverage numbers
- [[sources/codyschneider-email-generation-agent]] — generate + verify as zero-cost alternative
