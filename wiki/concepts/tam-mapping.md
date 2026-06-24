---
title: "TAM Mapping"
type: concept
tags: [tam, targeting, enrichment, icp, signal-infrastructure, gtm-engineering, tiering, account-based]
created: 2026-06-24
updated: 2026-06-24
sources: [codyschneider-tam-mapping]
---

# TAM Mapping

The practice of building a bottoms-up, account-level database of every company that could realistically buy from you — named, enriched, tiered, and maintained as a living operational asset. [[Cody Schneider]]'s framing: TAM is not a number on a slide. It's a list. The list is the product that all GTM activity runs on.

## The Core Reframe

Most B2B teams treat TAM as a sizing exercise done once for investors: "$40B addressable market." This number is useless for getting customers. The operational version is specific: not "mid-market SaaS in North America" but the actual 4,200 companies that fit, with data attached.

> "sequences, ads, abm — that's just how you work the list"

## Why It's High-Leverage Now

Two things recently converged to make TAM mapping accessible:

1. **Enrichment got cheap.** Waterfall stacks ([[LeadMagic]], [[Findymail]], [[Prospeo]], [[PDL]]) resolve firmographics and contacts at scale for pennies. Previously a multi-week data team project.
2. **AI researches at scale.** Soft qualifiers that once required a human reading a website (Do they run paid media? Do they have outbound motion? Are they hiring SDRs?) are now answerable programmatically per account.

## The 5-Step Process

### 1. Define ICP in Variables, Not Vibes

Firmographics + technographics + disqualifiers. The rule: **specific enough that a machine could sort accounts with it.** "Growing SaaS company" is a vibe. "SaaS, 50–200 employees, using Salesforce, hiring ≥2 AEs, no enterprise contract in play" is a variable set.

This is the same discipline as [[ICP Avatar]] — applied to account-level filtering rather than message construction.

### 2. Pull the Universe

Sources: Crunchbase (company profiles + funding), BuiltWith (technographics), [[Apollo]] (B2B contacts), custom scrapers. Strategy: **over-pull, then filter.** The cost of pulling extra accounts is low; the cost of missing accounts is a gap in your map.

### 3. Enrich + Qualify

Two parallel tracks:
- **Contact enrichment waterfall** — multi-provider stack to reach 85%+ contact coverage (see [[Enrichment Waterfall]])
- **AI research per account** — soft qualifier extraction at scale; answers the variables defined in Step 1

This is where the leverage lives. AI processes thousands of accounts at analyst-grade research depth.

### 4. Tier the Accounts

| Tier | Fit level | Outreach mode |
|------|-----------|--------------|
| 1 | Best fit — all variables met | Human-led; best copy; direct attention |
| 2 | Good fit — most variables met | Hybrid; AI drafts, human reviews |
| 3 | Marginal fit | Fully automated outbound |

Tiering routes effort. Tier 1 gets your best copy and direct attention. Tier 3 gets automated sequences. The map is what makes this routing possible.

### 5. Layer Signals on Top

Live triggers (funding rounds, hiring signals, tech installs, job changes) fire onto the base map. This is the critical step that makes signals actionable:

- **Without the map:** "A company got funded" = noise. Unknown fit, unknown tier.
- **With the map:** "Tier 1 account just got funded" = immediate routing into the right sequence.

> "a signal is noise until it lands on an account you already wanted"

## TAM Mapping as a Prerequisite for Signal Infrastructure

This is the insight most signal-focused GTM teams miss. [[Signal Infrastructure]] — Trigify, RB2B, Fibbler, Common Room — only produces value when signals land on accounts you already know you want. Without the base map, you're chasing signals blind.

The sequence is: **build the map first → then layer signals on top.**

## What the Map Enables

| GTM motion | How the map enables it |
|------------|----------------------|
| Cold email sequences | Target by tier; Tier 1 gets personalized copy |
| Paid ads (ABM) | Upload Tier 1/2 as custom audiences |
| LinkedIn outreach | Prioritize by tier; suppress Tier 3 from human effort |
| Signal routing | Signals route automatically to the tier's designated sequence |
| Performance tracking | Account-level attribution across channels |

## The Failure Mode

Most teams skip the map and go straight to "send 10k emails." Reply rates are garbage. The problem isn't the copy or the sequences — it's that the underlying account set is untargeted, untiered, and unenriched. Good outbound requires a good TAM.

## Tools

| Layer | Tools |
|-------|-------|
| Universe pull | Crunchbase, BuiltWith, [[Apollo]], scrapers |
| Contact enrichment | [[LeadMagic]], [[Findymail]], [[Prospeo]], [[PDL]] waterfall |
| AI research / qualification | Claude / AI agents |
| Signal layer on top | [[Trigify]], [[RB2B]], [[Fibbler]], funding/hiring feeds |

## Open Questions

- At what scale does the TAM mapping process itself need to be automated? Schneider describes it as "an afternoon" — but that assumes clean data sources and pre-built enrichment workflows. [low confidence on timeline for most teams]
- How do you handle TAM drift? Companies enter/exit ICP fit continuously (growth, pivots, acquisitions). The "living asset" claim implies ongoing maintenance — but the post doesn't specify how often to refresh. [unanswered]

## See Also

- [[sources/codyschneider-tam-mapping]] — primary source
- [[concepts/signal-infrastructure]] — runs on top of the TAM map; signals are noise without it
- [[concepts/enrichment-waterfall]] — the contact enrichment step inside TAM building
- [[concepts/icp-avatar]] — machine-sortable ICP variables = Step 1 of TAM mapping
- [[concepts/gtm-engineering]] — TAM mapping is the foundational infrastructure layer
- [[concepts/hybrid-ai-model]] — Tier 1 = human-led; Tier 3 = fully automated; same principle
- [[entities/leadmagic]] — enrichment provider
- [[entities/prospeo]] — enrichment provider
- [[entities/pdl]] — People Data Labs; firmographics + contacts at scale
