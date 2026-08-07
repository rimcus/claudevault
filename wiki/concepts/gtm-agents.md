---
title: "GTM Agents"
type: concept
tags: [ai-agents, gtm, marketing-automation, sales, growth]
created: 2026-04-14
updated: 2026-08-07
sources: [codyschneider-gtm-agents, codyschneider-twitter-outreach-pipeline, codyschneider-ai-ugc-ads, hridoyreh-saas-blueprint, codyschneider-marketing-agents-per-vertical, codyschneider-paid-ads-playbook, codyschneider-ai-search-seo, codyschneider-ai-media-company-playbook, codyschneider-ad-library-gap-analysis, codyschneider-seo-for-saas-101, codyschneider-ai-citation-loop]
---

# GTM Agents

Autonomous AI agents that run go-to-market workflows — lead generation, advertising management, SEO content production, CRM enrichment, email nurture — with minimal human involvement. Each agent is assigned a specific GTM function, given the relevant tool access and data, and runs continuously or on a schedule.

## Overview

GTM Agents represent the application of the [[LLM-Maintained Wiki]] insight to business operations: just as an LLM can maintain a wiki without human bookkeeping, it can run marketing and sales workflows without human execution. The human role shifts from doing the work to configuring the agents, reviewing outputs, and setting strategy.

[[Cody Schneider]]'s 2026 thread is the most concrete public blueprint for this: a minimum viable stack deployed in 10 minutes, with 8 specific agent workflows demonstrated.

## Minimum Viable Stack

| Component | Tool | Purpose |
|-----------|------|---------|
| Agent runtime | [[Hermes Agent]] on [[Hetzner]] VPS | Executes agents, always-on |
| LLM access | [[OpenRouter]] (MiniMax 2.7) | Intelligence layer |
| Data backbone | Open-source data warehouse | Context for decisions |

**The data warehouse is non-negotiable.** Agents making decisions without business data (conversion rates, campaign performance, user behavior) are guessing. The warehouse is what makes them genuinely useful.

## Implemented Agent Workflows

| Domain | Agent | Key Tools |
|--------|-------|-----------|
| Lead Gen | LinkedIn pipeline: scrape → enrich → verify → add to campaign | [[Apify]], [[Apollo]], [[Million Verifier]], [[Instantly]] |
| Paid Ads | Google Search Ads optimization | [[Ahrefs]] MCP, Search Console |
| Paid Ads | Facebook Ads creative management | Facebook Marketing API |
| CRM | HubSpot enrichment (hourly) | [[Exa API]], [[HubSpot]] |
| SEO | Landing page creation (3/day) | [[Ahrefs]] MCP, CMS API |
| Email | Nurture sequence optimization | [[SendGrid]] |
| SEO | Blog keyword → content → publish | [[Ahrefs]] MCP, CMS API, [[PostHog]] |

## Key Properties

- **Always-on:** agents run continuously on a VPS, not just when triggered manually
- **Data-grounded:** all decisions flow through the data warehouse
- **Chainable:** outputs of one agent become inputs of another (e.g. LinkedIn scrape → cold email campaign → inbox management)
- **Tool-composable:** each workflow is assembled from best-in-class point tools via APIs and MCPs

## Where GTM Agents Fit in the SaaS Lifecycle

Per [[Hridoy Rehman]]'s [[SaaS Lifecycle]] blueprint, GTM agents primarily automate:
- **Acquisition** (SEO, cold email, ads)
- **Retention** (email nurture, onboarding automation)
- **Analytics** (tracking, funnel analysis)
- **Revenue** (CRM enrichment supporting conversions)

The implication: a well-configured agent stack can run most of the post-launch SaaS revenue engine autonomously.

## SEO Agent Tactical Spec (June 2026)

From [[sources/codyschneider-ai-search-seo]], the two-lever SEO system the SEO agent executes:

**Lever 1 — Rank for bottom-of-funnel keywords:** Target "best X for Y / X alternative / tools like X" patterns. Scrape what's on page 1 → define product differentiation → write a post that includes your product and its differences → publish + sitemap. Pro tips: 100 pages per sitemap URL for faster indexing; minimize page size for crawl budget.

**Lever 2 — Acquire AI citations:** Use [[PromptWatch]] to map which citations AI search platforms (ChatGPT, Perplexity, etc.) use for target keywords → export and priority-rank by citation frequency → cold email site owners via [[Instantly]] requesting citation inclusion (expect paid placement) → prioritize spend on highest-frequency citations.

**The reframe:** AI search is not a new discipline — it is SEO with two levers. The SEO agent runs Lever 1 autonomously (keyword research, content, publish, sitemap). Lever 2 maps to the cold outreach agent with a different target list. See [[AI Search SEO]] for the full concept.

**Named-tool update (July 2026):** [[sources/codyschneider-seo-for-saas-101]] re-executes Lever 1 with specific tools — Claude Code + an SEO data API for keyword discovery, [[entities/serper|Serper]] for page-1 scraping — and adds one new step: a recorded founder video (or Claude-mobile-app interview) folded into the article alongside the competitor research, plus scroll-triggered CTA placement (first paragraph, 25/50/75%) tracked via [[entities/google-tag-manager|Google Tag Manager]] + [[entities/google-analytics-4|Google Analytics 4]] + [[entities/google-search-console|Google Search Console]]. See [[concepts/founder-perspective-content-moat]] for the durability argument behind the new step.

**Citation Shape Engineering (August 2026)** ([[sources/codyschneider-ai-citation-loop]])
[[entities/promptwatch|PromptWatch]] (find prompts you're losing, per-model) → [[entities/dataforseo|DataForSEO]] AI Optimization API (size the opportunity, live citations across 4 models) → [[entities/codex|Codex]] (fetch + structurally analyze top 20 cited URLs) → Claude Code (write content matching that structure, FAQPage + Article schema, CMS-ready JSON) → CMS API (publish 20-30 posts in one command) → [[entities/indexnow|IndexNow]] + Search Console (index) → re-run the same prompts in two weeks and check citation-array membership. The most technically detailed SEO agent spec in the wiki, and a structural (not outreach-based) alternative to Lever 2. See [[concepts/citation-shape-engineering]] for the full breakdown.

## Paid Ads Tactical Spec (June 2026)

From [[sources/codyschneider-paid-ads-playbook]], the simplest effective paid ads system for SaaS:

**Google Ads:** phrase match on bottom-of-funnel keywords → landing page H1/P1 = the keyword → conversion events for signup + payment.

**Facebook Ads:** broad targeting (all of Facebook) → test 10 creatives/week → isolate winners into dedicated conversion campaigns → landing page H1/P1 matches the ad → same conversion events.

**Measurement:** CAC vs CLV vs payback period via a dashboard ([[Graphed]] or Looker Studio). The one-number test: $1 in → $5 CLV out = scale. These are the feedback signals the Google Ads and Facebook Ads agents optimize against — not clicks or CPM.

**Simplicity principle:** most SaaS founders fail at paid ads by overcomplicating targeting. Simple intent matching (Google) + creative volume (Facebook) outperforms clever strategy.

## Additional Pipelines (Beyond the Core 8)

From subsequent Schneider threads:

**Twitter Outreach Pipeline** ([[sources/codyschneider-twitter-outreach-pipeline]])
Twitter post engagers → Exa AI (find LinkedIn) → Apollo (email) → Instantly (send) → [[Graphed]] (analyze)
The "inbound content outbound cold" strategy — people who engage with relevant content are pre-qualified leads.

**AI UGC Ads Pipeline** ([[sources/codyschneider-ai-ugc-ads]])
Reddit pain points (Exa AI) → Claude scripts → [[HeyGen]] video → ffmpeg + json2video (post-process) → FB Ads → [[Graphed]] + Stripe (CLV analysis) → remix winners → repeat
Produces 100+ ad variations per cycle; optimizes for Customer Lifetime Value, not just clicks.

**AI Media Company Playbook** ([[sources/codyschneider-ai-media-company-playbook]], July 2026)
A step change in scope from single-function agents to entire agent-run owned-media properties, monetized by ads for the operator's own product: [[concepts/directory-website-seo-play|directory website]] (Hermes scrape → Claude Code one-shot build → Vercel → Search Console), [[concepts/podcast-newsletter-growth-loop|podcast + newsletter]] (interview research → script → ElevenLabs TTS → Transistor.fm → newsletter), and [[concepts/tiktok-reel-farm|TikTok reel farm]] (DoubleSpeed AI account cohort → Nano Banana slideshows). See [[concepts/ai-media-company-playbook]] for the full breakdown.

**Competitor Creative Gap Analysis** ([[sources/codyschneider-ad-library-gap-analysis]], July 2026)
Apify (scrape competitor Facebook Ads Library) → Gemini (describe angle/promise/outcome) → Claude (find messaging gaps) → Exa AI (validate gap via Reddit) → Nano Banana + Seedance (generate gap-filling ads) → Facebook API (upload) → Graphed MCP in Claude Code (analyze performance, 1 day later) → Facebook API (kill losers, scale winners) → deploy to server. The clearest example yet in this wiki of an agent both analyzing performance data *and* directly executing the resulting budget decision via API, with no human step in between. See [[concepts/competitor-creative-gap-analysis]] for the full breakdown.

## Contradictions & Open Questions

- **[[Cold Email Personalization Problem]]:** As these pipelines become widespread, AI-generated emails converge on the same tone and structure, eliminating personalization advantage. Currently unsolved. [high confidence this is a real problem]
- What is the failure mode when agents chain incorrectly? No source yet addresses agent error recovery or human review checkpoints.
- How does this scale? The data warehouse approach is described as sufficient at startup scale — unclear at what point it breaks. [low confidence]
- MiniMax 2.7 is recommended by Schneider but no comparison against other models for GTM tasks exists yet.

## See Also

- [[sources/codyschneider-gtm-agents]] — the concrete implementation blueprint
- [[concepts/ai-media-company-playbook]] — owned-media extension of the same agents-run-GTM thesis
- [[concepts/competitor-creative-gap-analysis]] — competitor-intelligence extension; agent both analyzes and executes budget decisions
- [[concepts/founder-perspective-content-moat]] — named-tool SEO agent update; the founder-perspective step as durability layer
- [[concepts/citation-shape-engineering]] — structural citation-acquisition pipeline; most technically detailed SEO agent spec yet
- [[AI Marketing Stack]] — the infrastructure layer
- [[Data Warehouse for AI]] — the critical enabling component
- [[SaaS Lifecycle]] — the broader framework GTM agents fit into
- [[LLM-Maintained Wiki]] — the pattern GTM agents mirror (LLM doing human maintenance work)
- [[Agent Chaining]] — the compounding technique
