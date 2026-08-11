---
title: "Enrichment Waterfall"
type: concept
tags: [gtm, data, enrichment, targeting, clay]
created: 2026-04-14
updated: 2026-08-11
sources: [alexvacca-gtm-engineering-hire, salescaptain-linkedin-outbound-playbook, codyschneider-email-generation-agent, codyschneider-tam-mapping, codyschneider-two-agents-podcast]
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

## Enrichment in TAM Mapping (Schneider, June 2026)

[[sources/codyschneider-tam-mapping]] adds four providers to the enrichment landscape, positioned as the contact resolution layer within full TAM building (not just per-campaign enrichment):

- [[LeadMagic]] — firmographics + contacts at scale
- [[Findymail]] — already in wiki (1st-pass email)
- [[Prospeo]] — already referenced above
- [[PDL]] (People Data Labs) — large-scale B2B data; firmographics + contacts for high-volume pulls

Schneider also names a parallel enrichment track within TAM building: **AI research for soft qualifiers** — LLMs reading company websites and job postings to answer questions like "do they run paid media?" or "are they hiring SDRs?" This is qualitative enrichment that no data provider currently offers at scale.

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

## Aggregated Waterfalls: One Call Instead of a Manual Chain (Schneider, August 2026)

[[sources/codyschneider-two-agents-podcast]] introduces [[entities/origami|Origami]], an aggregator that sits in front of the waterfall pattern and exposes the entire cascade behind a single API call — the agent doesn't manually chain provider A → provider B → provider C; it calls Origami once and Origami handles the routing internally. This is a productization of the waterfall pattern itself, not a new provider in the chain.

The same post adds two more specifics to the existing waterfall:

- **[[LeadMagic]] named specifically for mobile phone number enrichment** — a narrower role than its general firmographic/contact use elsewhere in the wiki (see [[sources/codyschneider-tam-mapping]]).
- **[[entities/millionverifier|MillionVerifier]]** as the validation step immediately before sending — functionally the same role [[ZeroBounce]] plays in the SalesCaptain waterfall, confirming validation-before-send is a consistent requirement across every enrichment stack in this wiki, regardless of which specific provider does it.

**Sequencing rule:** ICP-fit research should happen *before* enrichment, not after — spend enrichment budget only on prospects that already pass qualification. See [[Signal Infrastructure]]'s LinkedIn Sourcing Mechanics section for the fuller context this rule comes from.

**Compliance note (new, previously unaddressed in this wiki):** buying broker contact data is legal, but usage rules differ — Schneider flags this without resolving it further. No enrichment page in this wiki previously addressed legal/compliance boundaries around purchased contact data; this is the first mention.

**Cost anchor:** roughly $200/month in total infrastructure spend (domains, inboxes, tooling) to start sending at 10k volume — see [[Cold Email Infrastructure]] for the domain/inbox side of that figure.

## Zero-Cost Alternative: Generate + Verify

[[Cody Schneider]] describes a zero-cost alternative to the paid first-pass: generate every plausible email pattern for a person + domain (given a LinkedIn profile), then existence-check via a cheap API (e.g., mailtester.ninja) and validate with a deliverability tool (MillionVerifier).

**Trade-off vs. paid first-pass:**

| Approach | Cost | Coverage | Limitation |
|----------|------|---------|-----------|
| Paid enrichment (Findymail) | ~$0.01–0.05/contact | ~50–60% | Paid |
| Generate + verify | Near-zero | ~60–70% of non-catch-all domains | Fails on catch-all domains |

**Critical caveat (from @MrColdEmail):** 30–40% of business domains are configured as catch-alls — any email combination returns "valid," making the existence-check step unreliable for those domains. Best suited for SMB campaigns where cost matters and enterprise catch-all domains are less common.

## See Also

- [[TAM Mapping]] — the broader process enrichment sits inside; the waterfall is Step 3 of TAM building
- [[Signal Infrastructure]] — the upstream layer that feeds the waterfall
- [[GTM Engineering]] — the practice that uses enrichment waterfalls
- [[Clay]] — where waterfalls are built
- [[Findymail]] — 1st-pass email enrichment provider
- [[ZeroBounce]] — validation layer (final step)
- [[Apollo]] — 3rd-pass enrichment provider
- [[sources/alexvacca-gtm-engineering-hire]] — Vacca's framework (8–12 data points)
- [[sources/salescaptain-linkedin-outbound-playbook]] — SalesCaptain's waterfall with coverage numbers
- [[sources/codyschneider-email-generation-agent]] — generate + verify as zero-cost alternative
- [[sources/codyschneider-two-agents-podcast]] — Origami aggregator, ICP-fit-before-enrichment ordering, broker-data compliance note
- [[entities/origami|Origami]] — waterfall aggregator, single-call abstraction
- [[entities/millionverifier|MillionVerifier]] — pre-send validation step
- [[Cold Email Infrastructure]] — the ~$200/month infrastructure cost this waterfall's spend sits alongside
