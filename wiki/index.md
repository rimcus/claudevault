---
title: "Index"
type: meta
updated: 2026-04-14
---

# Wiki Index

*Content catalog. Updated on every ingest. Read this first when answering queries — find relevant pages, then drill in.*

**Total pages:** 45 | **Sources ingested:** 6 | **Last updated:** 2026-04-14

---

## Sources

One page per ingested source. Links to raw file in `raw/sources/`.

- [[sources/karpathy-llm-wiki-pattern|LLM Wiki Pattern]] — Andrej Karpathy's founding gist defining the LLM-maintained wiki methodology (1 source)
- [[sources/codyschneider-gtm-agents|How to Build GTM Agents in 10 Minutes]] — Cody Schneider's concrete stack for autonomous AI marketing agents: Hermes + Hetzner + OpenRouter + data warehouse (1 source)
- [[sources/hridoyreh-saas-blueprint|The Complete SaaS Blueprint]] — Hridoy Rehman's 16-phase, ~85-node folder-tree map of the full SaaS lifecycle (1 source)
- [[sources/codyschneider-twitter-outreach-pipeline|Twitter Engager → Cold Outreach Pipeline]] — Schneider's earlier pipeline: Twitter engagers → Exa AI → Apollo → Instantly; introduces "inbound content outbound cold" strategy (1 source)
- [[sources/codyschneider-ai-ugc-ads|100+ AI UGC Ads for SaaS]] — Reddit pain points → Claude scripts → HeyGen video → FB Ads → CLV-optimized growth loop (1 source)
- [[sources/alexvacca-gtm-engineering-hire|The GTM Engineering Hire]] — Alex Vacca / ColdIQ: the definitive role definition, 4 pillars, hiring criteria, and build phases — backed by 400+ B2B engagements and 23M+ cold emails (1 source)

---

## Concepts

Topic and idea pages.

- [[concepts/llm-maintained-wiki|LLM-Maintained Wiki]] — the core pattern: LLM builds and maintains a persistent compounding wiki rather than doing RAG
- [[concepts/retrieval-augmented-generation|Retrieval-Augmented Generation]] — the contrasting approach; stateless retrieval from raw documents at query time
- [[concepts/knowledge-compounding|Knowledge Compounding]] — the property that makes LLM wikis more valuable over time than RAG systems
- [[concepts/memex|Memex]] — Vannevar Bush's 1945 vision of a personal associative knowledge store; the historical precedent
- [[concepts/schema-governed-llm-behavior|Schema-Governed LLM Behavior]] — using CLAUDE.md/AGENTS.md to make the LLM a disciplined, consistent wiki maintainer
- [[concepts/gtm-agents|GTM Agents]] — autonomous AI agents running go-to-market workflows (lead gen, ads, SEO, email nurture)
- [[concepts/saas-lifecycle|SaaS Lifecycle]] — the complete 16-phase map from idea to exit; the framework GTM agents operate within
- [[concepts/ai-marketing-stack|AI Marketing Stack]] — the minimum infrastructure for GTM agents: agent runtime + LLM gateway + data warehouse
- [[concepts/data-warehouse-for-ai|Data Warehouse for AI]] — centralizing business data so agents have context to make real decisions, not guesses
- [[concepts/gtm-engineering|GTM Engineering]] — the practice of building automated, code-driven GTM pipelines; treating marketing like software infrastructure
- [[concepts/ai-ugc-ads|AI UGC Ads]] — AI-generated UGC-style video ads at scale; 100+ variations per cycle, optimized for CLV
- [[concepts/growth-loop|Growth Loop]] — self-reinforcing optimization cycle: run → measure CLV → remix winners → repeat
- [[concepts/cold-email-personalization-problem|Cold Email Personalization Problem]] — confirmed by ColdIQ data: full AI autonomy erodes pipeline quality within one quarter; [[Hybrid AI Model]] is the mitigation
- [[concepts/signal-infrastructure|Signal Infrastructure]] — the upstream data layer (intent signals, hiring triggers, funding events) that makes campaigns smart over time; the layer most companies skip
- [[concepts/enrichment-waterfall|Enrichment Waterfall]] — multi-provider enrichment stacking to reach 8–12 data points per prospect before any email is sent
- [[concepts/hybrid-ai-model|Hybrid AI Model]] — AI on volume work + humans on judgment; empirically validated by ColdIQ across 400+ clients

---

## Entities

People, tools, organizations.

### People
- [[entities/andrej-karpathy|Andrej Karpathy]] — AI researcher; originator of the LLM wiki pattern
- [[entities/vannevar-bush|Vannevar Bush]] — engineer; proposed the Memex (1945)

### People
- [[entities/cody-schneider|Cody Schneider]] — growth practitioner; author of the GTM agents blueprint
- [[entities/hridoy-rehman|Hridoy Rehman]] — builder; author of the SaaS lifecycle blueprint

### Tools
- [[entities/obsidian|Obsidian]] — the markdown vault app serving as the browsing interface ("the IDE") for this wiki
- [[entities/qmd|qmd]] — optional local search engine for markdown (BM25/vector hybrid); for when the index isn't enough
- [[entities/hermes-agent|Hermes Agent]] — AI agent framework used as the runtime in Schneider's GTM stack
- [[entities/apify|Apify]] — web scraping platform; first step in the LinkedIn lead pipeline
- [[entities/apollo|Apollo]] — B2B contact enrichment; email finding from LinkedIn profiles
- [[entities/instantly|Instantly]] — cold email platform; final step in the lead pipeline + inbox management
- [[entities/graphed|Graphed]] — Cody Schneider's AI data analyst product; connects cold email + CRM + ads + Stripe for CLV analysis; closes the growth loop
- [[entities/heygen|HeyGen]] — AI video generation API; produces UGC-style ad videos from Claude-written scripts
- [[entities/alex-vacca|Alex Vacca]] — co-founder of ColdIQ; author of the GTM Engineering Hire guide; the empirical voice on what actually works in outbound at scale
- [[entities/coldiq|ColdIQ]] — GTM agency, $7M+ ARR, 400+ B2B clients, 23M+ emails; the data source behind Vacca's claims
- [[entities/clay|Clay]] — the central workflow-building tool for GTM engineers; enrichment waterfalls, signal processing, campaign orchestration

---

## Analyses

Query answers filed back into the wiki.

*None yet.*

---

## Meta

- [[overview]] — current synthesis and state of the knowledge base
- [[log]] — chronological record of all operations
