---
title: "Log"
type: meta
---

# Log

*Append-only. Most recent entries at the top. Each entry starts with `## [YYYY-MM-DD]` for grep-parseability.*

```bash
# Get last 10 entries:
grep "^## \[" wiki/log.md | head -10
```

---

## [2026-04-14] ingest | The GTM Engineering Hire (@itsalexvacca / ColdIQ)

- Summary page: [[sources/alexvacca-gtm-engineering-hire]]
- Raw source: `raw/sources/The GTM Engineering Hire_ A Comprehensive Guide...md`
- Pages created:
  - [[sources/alexvacca-gtm-engineering-hire]]
  - [[concepts/signal-infrastructure]]
  - [[concepts/enrichment-waterfall]]
  - [[concepts/hybrid-ai-model]]
  - [[entities/alex-vacca]]
  - [[entities/coldiq]]
  - [[entities/clay]]
- Pages updated:
  - [[concepts/gtm-engineering]] (major update: added 4 pillars, hiring criteria, Vacca's framework alongside Schneider's pipelines)
  - [[concepts/cold-email-personalization-problem]] (confirmed + quantified by ColdIQ data; added Hybrid AI Model as validated mitigation)
  - [[wiki/index.md]], [[wiki/overview.md]]
- Key takeaway: The most empirically grounded source in this wiki. Key claims backed by 400+ companies, 23M+ emails: (1) "The list is the strategy" — targeting quality #1 predictor of reply rate. (2) Full AI autonomy erodes pipeline quality within one quarter. (3) One GTM engineer replaces a 3-person SDR pod. (4) Signal infrastructure is the layer most companies skip.

---

## [2026-04-14] ingest | 100+ AI UGC Ads for SaaS (@codyschneider, Thread 3)

- Summary page: [[sources/codyschneider-ai-ugc-ads]]
- Raw source: `raw/sources/Thread by @codyschneider (3).md`
- Pages created:
  - [[sources/codyschneider-ai-ugc-ads]]
  - [[concepts/ai-ugc-ads]]
  - [[concepts/growth-loop]]
  - [[entities/heygen]]
- Pages updated: [[concepts/gtm-agents]] (added UGC pipeline), [[concepts/gtm-engineering]] (added pipeline), [[entities/graphed]], [[wiki/index.md]]
- Key takeaway: Reddit pain points → Claude scripts → HeyGen video → FB Ads → CLV-optimized [[Growth Loop]]. Optimizes for Customer Lifetime Value (Stripe), not just clicks. 100+ variations per cycle.

---

## [2026-04-14] ingest | Twitter Engager → Cold Outreach Pipeline (@codyschneider, Thread 2)

- Summary page: [[sources/codyschneider-twitter-outreach-pipeline]]
- Raw source: `raw/sources/Thread by @codyschneider (2).md`
- Pages created:
  - [[sources/codyschneider-twitter-outreach-pipeline]]
  - [[concepts/gtm-engineering]]
  - [[concepts/cold-email-personalization-problem]]
  - [[entities/graphed]]
- Pages updated: [[concepts/gtm-agents]] (added pipeline + opened personalization problem), [[wiki/index.md]]
- Key takeaway: Introduces "inbound content outbound cold" — Twitter engagers as pre-qualified leads. Community surfaced the [[Cold Email Personalization Problem]] as the real bottleneck: AI pipelines converging on identical-sounding emails.

---

## [2026-04-14] note | Thread by @codyschneider (1) is a duplicate

- Raw source: `raw/sources/Thread by @codyschneider (1).md`
- Same URL as original GTM agents thread (already ingested). No new content. No new pages created.

---

## [2026-04-14] ingest | The Complete SaaS Blueprint (@hridoyreh)

- Summary page: [[sources/hridoyreh-saas-blueprint]]
- Raw source: `raw/sources/Thread by @hridoyreh.md`
- Pages created:
  - [[sources/hridoyreh-saas-blueprint]]
  - [[concepts/saas-lifecycle]]
  - [[entities/hridoy-rehman]]
- Pages updated: [[concepts/gtm-agents]] (cross-referenced SaaS lifecycle phases), [[wiki/index.md]], [[wiki/overview.md]]
- Key takeaway: A 16-phase, ~85-node map of the full SaaS lifecycle. Doubles as an agent assignment map — every phase can be assigned to an autonomous AI agent. Distribution is the most commonly neglected phase.

---

## [2026-04-14] ingest | How to Build GTM Agents in 10 Minutes (@codyschneider)

- Summary page: [[sources/codyschneider-gtm-agents]]
- Raw source: `raw/sources/Thread by @codyschneider.md`
- Pages created:
  - [[sources/codyschneider-gtm-agents]]
  - [[concepts/gtm-agents]]
  - [[concepts/ai-marketing-stack]]
  - [[concepts/data-warehouse-for-ai]]
  - [[entities/cody-schneider]]
  - [[entities/hermes-agent]]
  - [[entities/apify]]
  - [[entities/apollo]]
  - [[entities/instantly]]
- Pages updated: [[wiki/index.md]], [[wiki/overview.md]]
- Key takeaway: The minimum viable GTM agent stack is Hermes + Hetzner + OpenRouter + data warehouse. The data warehouse is the non-obvious critical ingredient. 8 concrete workflows demonstrated; chaining them is where the value compounds.

---

## [2026-04-14] ingest | LLM Wiki Pattern (Andrej Karpathy)

- Summary page: [[sources/karpathy-llm-wiki-pattern]]
- Raw source: `raw/sources/karpathy-llm-wiki-pattern.md`
- Pages created:
  - [[sources/karpathy-llm-wiki-pattern]]
  - [[concepts/llm-maintained-wiki]]
  - [[concepts/retrieval-augmented-generation]]
  - [[concepts/knowledge-compounding]]
  - [[concepts/memex]]
  - [[concepts/schema-governed-llm-behavior]]
  - [[entities/andrej-karpathy]]
  - [[entities/obsidian]]
  - [[entities/vannevar-bush]]
  - [[entities/qmd]]
- Pages updated: *(first ingest — none pre-existing)*
- Infrastructure created: CLAUDE.md, wiki/index.md, wiki/log.md, wiki/overview.md, all templates
- Key takeaway: This vault instantiates the LLM-maintained wiki pattern — the founding source documents the methodology the vault itself operates on.

---

## [2026-04-14] setup | Vault initialized

- Created directory structure: `wiki/`, `raw/`, `templates/`
- Created schema: `CLAUDE.md`
- Created templates: source-summary, concept, entity, analysis
- First source queued for ingest: Karpathy LLM Wiki gist
