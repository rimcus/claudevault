---
title: "TAM Mapping: The Highest-Leverage Thing in B2B Right Now"
type: source
tags: [tam, targeting, enrichment, icp, signal-infrastructure, gtm-engineering, tiering]
created: 2026-06-24
updated: 2026-06-24
sources: [codyschneider-tam-mapping]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2069767512888143889"
source_type: x-post
---

# TAM Mapping: The Highest-Leverage Thing in B2B Right Now

**Author:** [[Cody Schneider]] (@codyschneider)
**Published:** 2026-06-24
**Context:** Playbook post on TAM mapping as an operational GTM asset. The foundational piece beneath the entire Schneider GTM stack — the base map that signals, sequences, ads, and ABM all run on. Published same day, June 24, as the most recent post in this wiki.

---

## Core Thesis

TAM is not a slide number. It's a list. Specifically, it's a bottoms-up, account-level database of every company that could realistically buy from you — named, enriched, tiered. The "$40B market" figure on slide 12 is useless for getting customers. The actual 4,200 companies that fit, with data attached, is your GTM foundation.

> "TAM isn't a sizing exercise you do once for investors. it's a living asset your whole GTM sits on. the list is the product."

Most teams skip the map and go straight to "send 10k emails" — then wonder why reply rates are garbage. You can't run good outbound on a bad TAM.

---

## Why Now

Two things converged:

1. **Enrichment got cheap and good.** Waterfall stacks — [[LeadMagic]], [[Findymail]], [[Prospeo]], [[PDL]] — resolve firmographics and contacts at scale for pennies. Five years ago this was a data team project. Now it's an afternoon.

2. **AI researches at scale.** Run every account through a research step; pull the soft qualifiers that used to require a human reading the website: Do they run paid media? Do they have an outbound motion? Are they hiring SDRs? All answerable programmatically now.

---

## The 5-Step Process

### Step 1: Define ICP in Variables, Not Vibes

Firmographics + technographics + disqualifiers. Specific enough that **a machine could sort accounts with it**. "Mid-market SaaS in North America" is a vibe. "SaaS companies, 50–200 employees, using Salesforce, hiring ≥2 AEs, no enterprise contract in play" is a variable set.

This is the machine-sortable version of the [[ICP Avatar]] — same discipline applied to account-level filtering rather than message construction.

### Step 2: Pull the Universe

Sources:
- **Crunchbase** — company profiles, funding data
- **BuiltWith** — technographic data (what software a company runs)
- **[[Apollo]]** — B2B contact database
- **Scrapers** — custom scraping for niche signals

Strategy: **over-pull, then filter down.** Better to start with too many accounts and eliminate than to miss companies that belong in the map.

### Step 3: Enrich + Qualify

Two parallel tracks:
- **Waterfall enrichment** for contacts (see [[Enrichment Waterfall]])
- **AI research** for soft qualifiers — the machine reads the website, job postings, and public signals to answer the qualifier questions defined in Step 1

This is where the leverage lives. AI can process thousands of accounts at a research depth that previously required an SDR or analyst.

### Step 4: Tier It

Score each account 1/2/3 on fit:

| Tier | Fit | Effort level |
|------|-----|-------------|
| Tier 1 | Best fit | Human-led outreach |
| Tier 2 | Good fit | Hybrid (AI + human touch) |
| Tier 3 | Marginal fit | Fully automated outbound |

The tiering is what makes the map operational — it routes effort appropriately. Tier 1 gets your best copy and direct attention. Tier 3 gets automated sequences.

### Step 5: Layer Signals on Top

Live triggers (hiring, funding, tech installs, job changes) fire onto the base map. The result:

- **Without the map:** "Someone got funded" → noise. Who? Do they fit? Should you care?
- **With the map:** "Tier 1 account just got funded" → immediate routing into the right sequence

> "a signal is noise until it lands on an account you already wanted"

This is the missing prerequisite for [[Signal Infrastructure]]. Signals are only as good as the map they land on.

---

## The Shift in Mental Model

| Old TAM | New TAM |
|---------|---------|
| Sizing exercise (done once, for investors) | Living operational asset |
| Number on slide 12 | Named account database |
| "$40B market" | "4,200 specific companies, enriched, tiered" |
| Input to fundraising deck | Foundation for sequences, ads, ABM |

---

## Tools Named

| Purpose | Tools |
|---------|-------|
| Contact enrichment waterfall | [[LeadMagic]], [[Findymail]], [[Prospeo]], [[PDL]] |
| Universe pull | Crunchbase, BuiltWith, [[Apollo]], scrapers |
| AI research at scale | Claude / AI agents |
| Signal layer | Hiring signals, funding events, tech installs, job changes |

---

## Entities Mentioned

- [[LeadMagic]] — enrichment provider
- [[Findymail]] — enrichment provider (1st-pass, already in wiki)
- [[Prospeo]] — enrichment provider (already referenced in wiki, now has entity page)
- [[PDL]] (People Data Labs) — data provider; firmographics + contacts at scale
- [[Apollo]] — B2B contact database; universe pull layer
- [[Graphed]] — promoted as the implementation service

## Concepts Touched

- [[TAM Mapping]] — the core concept this post defines
- [[Signal Infrastructure]] — signals need a base map; TAM mapping is the prerequisite
- [[Enrichment Waterfall]] — the contact enrichment step within TAM building
- [[ICP Avatar]] — machine-sortable ICP variables = Step 1 of TAM mapping
- [[GTM Engineering]] — TAM mapping is the foundational GTM infrastructure
- [[Hybrid AI Model]] — AI for Tier 3 automated outbound; humans for Tier 1

## See Also

- [[concepts/tam-mapping]] — the extracted concept
- [[concepts/signal-infrastructure]] — what runs on top of the TAM map
- [[concepts/enrichment-waterfall]] — the contact enrichment step inside TAM building
- [[concepts/icp-avatar]] — machine-sortable ICP definition as the TAM entry gate
- [[concepts/gtm-engineering]] — the practice context
- [[entities/leadmagic]] — new enrichment provider
- [[entities/prospeo]] — enrichment provider
- [[entities/pdl]] — People Data Labs
