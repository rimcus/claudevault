---
title: "Index"
type: meta
updated: 2026-04-14
---

# Wiki Index

*Content catalog. Updated on every ingest. Read this first when answering queries — find relevant pages, then drill in.*

**Total pages:** 97 | **Sources ingested:** 18 | **Last updated:** 2026-06-16

---

## Sources

One page per ingested source. Links to raw file in `raw/sources/`.

- [[sources/karpathy-llm-wiki-pattern|LLM Wiki Pattern]] — Andrej Karpathy's founding gist defining the LLM-maintained wiki methodology (1 source)
- [[sources/codyschneider-gtm-agents|How to Build GTM Agents in 10 Minutes]] — Cody Schneider's concrete stack for autonomous AI marketing agents: Hermes + Hetzner + OpenRouter + data warehouse (1 source)
- [[sources/hridoyreh-saas-blueprint|The Complete SaaS Blueprint]] — Hridoy Rehman's 16-phase, ~85-node folder-tree map of the full SaaS lifecycle (1 source)
- [[sources/codyschneider-twitter-outreach-pipeline|Twitter Engager → Cold Outreach Pipeline]] — Schneider's earlier pipeline: Twitter engagers → Exa AI → Apollo → Instantly; introduces "inbound content outbound cold" strategy (1 source)
- [[sources/codyschneider-ai-ugc-ads|100+ AI UGC Ads for SaaS]] — Reddit pain points → Claude scripts → HeyGen video → FB Ads → CLV-optimized growth loop (1 source)
- [[sources/alexvacca-gtm-engineering-hire|The GTM Engineering Hire]] — Alex Vacca / ColdIQ: the definitive role definition, 4 pillars, hiring criteria, and build phases — backed by 400+ B2B engagements and 23M+ cold emails (1 source)
- [[sources/salescaptain-claude-code-gtm-playbook|Claude Code for GTM Playbook]] — Bill Stathopoulos / SalesCaptain: 12 playbooks, 8-step pipeline, ICP Avatar framework, CLAUDE.md as GTM engine; $50–150/month to run 2–4 campaigns (1 source)
- [[sources/salescaptain-linkedin-outbound-playbook|LinkedIn Outbound Playbook 2026]] — Bill Stathopoulos / SalesCaptain: $1M+ pipeline, 7 signal-triggered workflows, 8 data-backed DM principles from 120K+ DMs, content + outbound flywheel (1 source)
- [[sources/squeezeandscale-lemlist-email-nurturing|Email Marketing Data-Driven chez Lemlist]] — Squeeze and SCALE podcast (Spicy Lemon): Nicolas (Lemlist growth marketer) details the shift from temporal to behavioral email flows — 800+ demos, +4pts conversion, 600+ reviews, -40% churn (1 source, French)
- [[sources/anon-cold-email-systems-guide|The Comprehensive Guide to Scalable B2B Cold Email Systems]] — Anonymous practitioner guide: 9-chapter system covering infrastructure (20/day speed limit), KPIs (1 deal/10K prospects), Meat/Potatoes/Toppings copywriting, pay-per-call pricing, and Spin Tax Rule
- [[sources/anon-cold-email-copy-playbook|Cold Email Copy Playbook]] — Anonymous Notion playbook: 5 psychological triggers, 4-element structure, subject line data (38% open rate for question + company name), Friction Test for CTAs, 9 copy templates, ACV-based segmentation, 5-email follow-up sequence (65% of replies come from emails 2–5)
- [[sources/nickabraham-claude-code-campaign-lists|Claude Code for Cold Email Campaign Lists]] — Nick Abraham thread: Claude Code + Discolike MCP for campaign list management at scale; org hierarchy intelligence; 5 hours → 2 hours weekly; "MCP quality is the ceiling"
- [[sources/codyschneider-email-generation-agent|Build an AI Agent to Get Anyone's Email for Free]] — Cody Schneider post: generate every email pattern from LinkedIn + existence-check via cheap API + validate; zero-cost alternative to paid enrichment; catch-all domain caveat (30–40% of domains)
- [[sources/codyschneider-marketing-agents-per-vertical|Deploy Marketing Agents Per Vertical With Live Business Data]] — Cody Schneider post: agent-per-vertical model; Airbyte + ClickHouse named as open-source warehouse stack; agents write their own skill files (self-compounding); Graphed repositioned as a service (5-day implementation)
- [[sources/codyschneider-paid-ads-playbook|Stop Overcomplicating Paid Ads for SaaS]] — Cody Schneider post: Google (bottom-of-funnel phrase match) + Facebook (10 creatives/week, isolate winners) + CLV-based measurement; the tactical spec for the paid ads GTM agents
- [[sources/theory-fb-ads-library-claude-saas|[METHOD] FB Ads Library + Claude = $$$]] — BlackHatWorld practitioner post: Facebook Ads Library → Claude scoring → Lovable-ready prompt → MVP in ~10 days; £2,950 MRR across 6 tools; the market-validation-first build methodology
- [[sources/codyschneider-ai-search-seo|Stop Overcomplicating This: AI Search Is Just SEO]] — Cody Schneider post: two-lever framework (rank page 1-3 for comparison keywords + acquire AI citations via PromptWatch + Instantly); the tactical spec for the SEO agent
- [[sources/codyschneider-fb-ads-ugc-playbook|Facebook Ads for SaaS 101]] — Cody Schneider post: Perplexity + Reddit quotes → Claude scripts → HeyGen/Seedance/Veo3 video → click campaign (7 days) → conversion campaign; Business Page Admin targeting; GTM conversion tracking detail

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
- [[concepts/signal-infrastructure|Signal Infrastructure]] — the upstream data layer (intent signals, hiring triggers, funding events, LinkedIn engagement) that makes campaigns smart over time; includes 7 LinkedIn-specific signal workflows
- [[concepts/enrichment-waterfall|Enrichment Waterfall]] — multi-provider enrichment stacking to reach 85%+ email coverage; specific providers and coverage numbers from SalesCaptain
- [[concepts/hybrid-ai-model|Hybrid AI Model]] — AI on volume work + humans on judgment; empirically validated by ColdIQ; three-column framework from SalesCaptain
- [[concepts/icp-avatar|ICP Avatar]] — 3-level pain hierarchy (surface → operational → identity-level); every phrase must come from exact customer quotes; the upstream fix for generic AI copy
- [[concepts/content-outbound-flywheel|Content Outbound Flywheel]] — LinkedIn content pre-warms prospects before outreach; two buyer journeys reinforcing each other; 79% ICP fit on inbound
- [[concepts/behavioral-email-triggers|Behavioral Email Triggers]] — triggering lifecycle emails on product actions rather than time-since-signup; the core architecture behind Lemlist's email marketing transformation
- [[concepts/cold-email-infrastructure|Cold Email Infrastructure]] — the domain/inbox/warm-up architecture; 20 emails/day speed limit; how to scale volume by adding inboxes not rate
- [[concepts/cold-email-copywriting|Cold Email Copywriting]] — Meat/Potatoes/Toppings framework; 4 personalization scenarios; Spin Tax Rule; Loom video strategy; subject line psychology
- [[concepts/ad-library-market-validation|Ad Library Market Validation]] — using Facebook Ads Library ad longevity as demand proof before building; Claude scores for SaaS recurring potential; Lovable builds the MVP; ~10 days idea-to-MRR
- [[concepts/ai-search-seo|AI Search SEO]] — AI search is just SEO with two levers: rank page 1-3 for comparison keywords, and acquire citations from sources AI search already trusts; PromptWatch maps the citation landscape

---

## Entities

People, tools, organizations.

### People
- [[entities/andrej-karpathy|Andrej Karpathy]] — AI researcher; originator of the LLM wiki pattern
- [[entities/vannevar-bush|Vannevar Bush]] — engineer; proposed the Memex (1945)
- [[entities/cody-schneider|Cody Schneider]] — growth practitioner; author of the GTM agents blueprint
- [[entities/hridoy-rehman|Hridoy Rehman]] — builder; author of the SaaS lifecycle blueprint
- [[entities/alex-vacca|Alex Vacca]] — co-founder of ColdIQ; author of the GTM Engineering Hire guide; the empirical voice on what actually works in outbound at scale
- [[entities/bill-stathopoulos|Bill Stathopoulos]] — CEO & co-founder of SalesCaptain; author of Claude Code for GTM and LinkedIn Outbound playbooks

### Organizations
- [[entities/coldiq|ColdIQ]] — GTM agency, $7M+ ARR, 400+ B2B clients, 23M+ emails; the data source behind Vacca's claims
- [[entities/salescaptain|SalesCaptain]] — GTM agency; $1M+ LinkedIn pipeline, 79% ICP fit; implementation-focused (Claude Code + LinkedIn workflows)

### Tools
- [[entities/obsidian|Obsidian]] — the markdown vault app serving as the browsing interface ("the IDE") for this wiki
- [[entities/qmd|qmd]] — optional local search engine for markdown (BM25/vector hybrid); for when the index isn't enough
- [[entities/hermes-agent|Hermes Agent]] — AI agent framework used as the runtime in Schneider's GTM stack
- [[entities/apify|Apify]] — web scraping platform; first step in the LinkedIn lead pipeline
- [[entities/apollo|Apollo]] — B2B contact enrichment; email finding from LinkedIn profiles; 3rd-pass in enrichment waterfall
- [[entities/instantly|Instantly]] — cold email platform; final step in the lead pipeline + inbox management
- [[entities/graphed|Graphed]] — Cody Schneider's AI data analyst product; connects cold email + CRM + ads + Stripe for CLV analysis; closes the growth loop
- [[entities/heygen|HeyGen]] — AI video generation API; produces UGC-style ad videos from Claude-written scripts
- [[entities/clay|Clay]] — the central workflow-building tool for GTM engineers; enrichment waterfalls, signal processing, LinkedIn workflow orchestration
- [[entities/heyreach|HeyReach]] — LinkedIn outreach platform; flat-fee unlimited profiles; execution layer in 5 of SalesCaptain's 7 workflows
- [[entities/lemlist|Lemlist]] — multichannel outreach (email + LinkedIn + WhatsApp); alternative to HeyReach when multi-channel sequences needed
- [[entities/trigify|Trigify]] — LinkedIn signal platform; detects post engagers, keyword activity, and profile interactions in real time
- [[entities/teamfluence|Teamfluence]] — LinkedIn profile viewer tracking; identifies who checks your profile before they act
- [[entities/fibbler|Fibbler]] — LinkedIn ad engager detection; surfaces prospects who engaged with ads but never clicked
- [[entities/rb2b|RB2B]] — website visitor deanonymization from LinkedIn traffic; closes loop between content and outbound
- [[entities/findymail|Findymail]] — 1st-pass email enrichment; cheapest provider, ~50–60% coverage
- [[entities/zerobounce|ZeroBounce]] — email validation; final step in enrichment waterfall before sending
- [[entities/customer-io|Customer.io]] — ESP + behavioral segmentation platform; central tool in Lemlist's lifecycle email stack; recommended at 1000+ users
- [[entities/spicy-lemon|Spicy Lemon]] — French B2B content agency; producer of the Squeeze and SCALE podcast
- [[entities/nick-abraham|Nick Abraham]] — cold email practitioner at scale (15+ campaigns); Claude Code + MCP workflow author
- [[entities/discolike|Discolike]] — MCP provider connecting Claude Code to contact databases
- [[entities/airbyte|Airbyte]] — open-source data pipeline; extraction and loading layer in the Airbyte + ClickHouse warehouse stack
- [[entities/clickhouse|ClickHouse]] — open-source columnar database; storage and query layer in Schneider's recommended GTM agent data warehouse stack
- [[entities/lovable|Lovable]] — AI app builder; generates 75–80% of a full-stack SaaS MVP from a single Claude-written prompt in one session
- [[entities/higgsfield|Higgsfield]] — MCP connector for image generation and structured visual output; enriches Claude prompts before passing to Lovable
- [[entities/promptwatch|PromptWatch]] — citation intelligence tool; identifies which sources AI search platforms use for a given category of queries
- [[entities/seedance|Seedance]] — AI video generation tool; alternative to HeyGen for UGC-style ad production
- [[entities/veo3|Veo3]] — Google's AI video generation model; used in the UGC ad pipeline alongside HeyGen and Seedance

---

## Analyses

Query answers filed back into the wiki.

*None yet.*

---

## Meta

- [[overview]] — current synthesis and state of the knowledge base
- [[log]] — chronological record of all operations
