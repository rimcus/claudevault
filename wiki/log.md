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

## [2026-08-07] ingest | Cody Schneider — AI Citation Loop / Citation Shape Engineering (X post)

- Summary page: [[sources/codyschneider-ai-citation-loop]]
- Raw source: `raw/sources/Post by @codyschneider on X 7.md` (short enough for git; not renamed)
- Pages created:
  - [[sources/codyschneider-ai-citation-loop]]
  - [[concepts/citation-shape-engineering]]
  - [[entities/dataforseo]]
  - [[entities/codex]]
  - [[entities/indexnow]]
- Pages updated:
  - [[entities/promptwatch]] (added API detail: per-model citation tracking, agent-crawler analytics, prompt-gap technique)
  - [[entities/graphed]] (added fourth positioning: Graphed CLI deploying paid ads/outbound/SEO agents together)
  - [[concepts/ai-search-seo]] (added structural alternative to Lever 2's outreach-based citation acquisition; flagged as unreconciled with existing Lever 2)
  - [[concepts/founder-perspective-content-moat]] (flagged unreconciled tension: this post's pure mechanical shape-matching vs. that concept's personal-perspective-as-moat argument, from the same author ~10 days apart)
  - [[concepts/gtm-agents]] (added as third, most technically detailed SEO agent spec)
  - [[entities/cody-schneider]] (added as seventh contribution area)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: The most technically dense Schneider post in the wiki — the first to name specific API endpoints (DataForSEO's `ai_optimization` family), a literal agent prompt, and structured-data requirements (FAQPage + Article schema), and the first to name a coding agent other than Claude Code (Codex, for the fetch-and-analyze step). Its central claim, "models retrieve chunks, not pages," reframes AI-search citation as a structural property of content — earnable by reverse-engineering and matching the shape of already-cited pages — rather than something bought via outreach (the wiki's existing Lever 2) or won through personal authenticity (the prior Schneider ingest's founder-perspective argument, published ~10 days earlier). Neither prior post is acknowledged or reconciled here; the wiki now holds three distinct, non-overlapping theories of what makes content win in AI search, from the same author, none of which are cross-referenced by Schneider himself. As with the two prior Schneider ingests, no before/after results are given — treat the method as directional.

---

## [2026-07-28] ingest | Cody Schneider — SEO for SaaS 101 (X post)

- Summary page: [[sources/codyschneider-seo-for-saas-101]]
- Raw source: `raw/sources/Post by @codyschneider on X 6.md` (short enough for git; not renamed)
- Pages created:
  - [[sources/codyschneider-seo-for-saas-101]]
  - [[concepts/founder-perspective-content-moat]]
  - [[entities/serper]]
  - [[entities/google-analytics-4]]
  - [[entities/google-tag-manager]]
- Pages updated:
  - [[concepts/ai-search-seo]] (added named-tool version of Lever 1 with the founder-perspective step and updated conversion-tracking detail)
  - [[concepts/gtm-agents]] (added named-tool SEO agent update to the existing SEO Agent Tactical Spec section)
  - [[concepts/founder-brand-strategy]] (cross-referenced convergent authenticity-as-moat argument from a second domain)
  - [[concepts/seo-mini-tools]] (cross-referenced as a third content-durability variant)
  - [[concepts/ai-ugc-ads]] (linked existing Google Tag Manager mention to its new entity page)
  - [[entities/google-search-console]] (added second use case: conversion-tracking stack)
  - [[entities/cody-schneider]] (added as sixth contribution area)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: Eight of this post's nine steps restate the wiki's existing AI Search SEO Lever 1 framework with specific tools named (Claude Code + an SEO API, Serper) rather than adding anything new. The one genuinely new step — recording a 30-minute founder video, or having the Claude mobile app interview the founder, and writing the article from that plus competitor research — is also the one a reply to the post (not Schneider) identifies as the actual point: once the mechanical steps are commoditized by widespread adoption of the same playbook, the founder's own perspective is the one input an LLM can't synthesize from the other ranking pages. This connects two previously unlinked wiki threads — the seo-mini-tools engineering-effort durability argument and the founder-brand-strategy authenticity argument — as a third variant of the same claim, now applied specifically to written SEO content. Like the prior Schneider ingest, this post has zero supporting metrics; treat the method as directional.

---

## [2026-07-28] ingest | Cody Schneider — Competitor Ad Library Gap Analysis (X post)

- Summary page: [[sources/codyschneider-ad-library-gap-analysis]]
- Raw source: `raw/sources/Post by @codyschneider on X 5.md` (short enough for git; not renamed)
- Pages created:
  - [[sources/codyschneider-ad-library-gap-analysis]]
  - [[concepts/competitor-creative-gap-analysis]]
  - [[entities/exa-ai]] (backfilled — recurs across 3 prior Schneider sources but never had its own page)
  - [[entities/gemini]]
- Pages updated:
  - [[entities/apify]] (added third pipeline role: competitor ad creative scraping)
  - [[entities/graphed]] (added MCP-into-Claude-Code autonomous performance-analysis role)
  - [[entities/seedance]], [[entities/nano-banana]] (added second use case: gap-filling ad creative generation)
  - [[entities/cody-schneider]] (added as fifth contribution area)
  - [[concepts/ai-ugc-ads]] (added as third research-source variant + more autonomous closing loop)
  - [[concepts/ad-library-market-validation]] (cross-referenced: same data source, different extraction target — longevity vs. message content)
  - [[concepts/gtm-agents]] (added as new pipeline instance; flagged as clearest analyze-and-execute example yet)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: This post inverts the research order of Schneider's prior ad pipelines — instead of starting from customer pain (Reddit, sales transcripts), it starts from what competitors are already claiming (Facebook Ads Library creative, described at the angle/promise/outcome level by Gemini), has Claude find the gap in category messaging, and only then validates that gap against Reddit. It's also the sharpest example yet in this wiki of an agent analyzing its own performance data and executing the resulting decision with no human step between the two: Graphed's MCP feeds Claude Code performance data, and Claude itself calls the Facebook Ads API to kill losers and reallocate budget, before the whole loop is deployed to a server to run unattended. Notably the only Schneider source in the wiki with zero supporting metrics (no CTR, spend, or revenue figure) — treat the method as directional, not validated.

---

## [2026-07-22] ingest | SaaS Connection — Maxime Champoux (Well): Building an AI-Native Engineering Org

- Summary page: [[sources/maximechampoux-well-ai-native-engineering]]
- Raw source: pasted transcript (French podcast, no file saved to raw/sources/ — ingested directly from chat)
- Pages created:
  - [[sources/maximechampoux-well-ai-native-engineering]]
  - [[concepts/toyota-production-system-for-software]]
  - [[concepts/business-context-graph]]
  - [[concepts/ai-native-engineering-team]]
  - [[concepts/design-code-inversion]]
  - [[concepts/agent-specialization-context-window]]
  - [[concepts/marginal-gains-1-percent]]
  - [[concepts/roadmap-abstraction-shift]]
  - [[entities/maxime-champoux]]
  - [[entities/alex-olivet]]
  - [[entities/well]]
  - [[entities/qonto]]
  - [[entities/ibanfirst]]
- Pages updated:
  - [[concepts/schema-governed-llm-behavior]] (added convergent evidence: Well's in-codebase skills/documentation is the same pattern applied to a production codebase)
  - [[concepts/product-engineers-no-pms]] (added convergent evidence: Champoux's roadmap-abstraction account vs. Harries' no-PM account — same trend, different mechanism)
  - [[concepts/data-warehouse-for-ai]] (added the SMB-scale variant: Well's business context graph as the same centralization thesis for a segment that can't afford a real warehouse)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: This is the wiki's first source on AI-native *software engineering* process itself, distinct from both the cold-email/GTM-agent core and the general growth-marketing layer added by the ElevenLabs source. Its most valuable material is the one part most public AI-coding accounts skip: a specific, dated quality plateau (a 12-person team stuck at 40-50 shipped features/month) and its root cause ("integrated but not assimilated" code — an AI agent unaware of a codebase's non-obvious historical "patina" takes a shortcut that reintroduces a fixed regression) and its fix (8 named, stable, domain-specialized agents with deliberately bounded context, orchestrated by an intent-reading dispatcher, with a generalizable heuristic: specialize once task material exceeds what a single context window can responsibly hold). This converges strongly with two concepts already in the wiki — [[concepts/schema-governed-llm-behavior]] and [[concepts/gtm-agents]]' "agents write their own skill files" pattern — as independent evidence that bounded, named, self-documenting agents are the emerging default architecture across GTM, product management, and core engineering alike. Several proper nouns are ambiguous due to French auto-transcription artifacts (flagged inline with confidence markers); none of the core operational claims depend on getting them exactly right.

---

## [2026-07-17] ingest | Cody Schneider — AI Media Company Playbook (X post)

- Summary page: [[sources/codyschneider-ai-media-company-playbook]]
- Raw source: renamed to `raw/sources/codyschneider-ai-media-company-playbook.md` (original filename was the full tweet text, too long for git)
- Pages created:
  - [[sources/codyschneider-ai-media-company-playbook]]
  - [[concepts/ai-media-company-playbook]]
  - [[concepts/directory-website-seo-play]]
  - [[concepts/podcast-newsletter-growth-loop]]
  - [[concepts/tiktok-reel-farm]]
  - [[entities/vercel]]
  - [[entities/google-search-console]]
  - [[entities/transistor-fm]]
  - [[entities/doublespeed-ai]]
  - [[entities/nano-banana]]
- Pages updated:
  - [[entities/cody-schneider]] (added the media-company playbook as a fourth contribution area)
  - [[entities/hermes-agent]] (added directory-site scraping use case)
  - [[entities/elevenlabs]] (added second, unrelated usage context: third-party TTS production tool vs. the company profiled in the Harries growth playbook)
  - [[concepts/gtm-agents]] (added media-company pipelines as a fourth "additional pipeline" category)
  - [[concepts/seo-mini-tools]], [[concepts/ai-search-seo]] (cross-referenced the new directory-website concept)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: Schneider reframes prior isolated GTM tactics (SEO, content, social) as pieces of a business running its own agent-operated media property — a directory site, a podcast + newsletter, or a TikTok account cohort — whose sole job is to build an audience the business then advertises its own product into. All three pipelines are described as agent-run end to end (Hermes/Claude Code for the directory scrape-and-build, an agent + ElevenLabs + Transistor.fm for the podcast, DoubleSpeed AI + Nano Banana for the TikTok cohort), with the human role limited to plan-mode direction and prompting. The post is terse and every headline metric (100 clicks/day, 20K list in 6 months, 300K impressions at $3 CPM) is a single-source, unverified claim — treat directionally, not as validated benchmarks.

---

## [2026-07-15] ingest | The $3.3B Growth Engine Behind ElevenLabs (Luke Harries, 20VC/20 Growth)

- Summary page: [[sources/lukeharries-elevenlabs-growth-playbook]]
- Raw source: `raw/sources/transcript.md`
- Pages created:
  - [[sources/lukeharries-elevenlabs-growth-playbook]]
  - [[concepts/launch-playbook]]
  - [[concepts/growth-video-strategy]]
  - [[concepts/counter-positioning]]
  - [[concepts/sharded-growth-teams]]
  - [[concepts/growth-hiring-order]]
  - [[concepts/cac-payback-period]]
  - [[concepts/product-engineers-no-pms]]
  - [[concepts/seo-mini-tools]]
  - [[concepts/founder-brand-strategy]]
  - [[entities/luke-harries]]
  - [[entities/elevenlabs]]
  - [[entities/mati-staniszewski]]
  - [[entities/harry-stebbings]]
- Pages updated:
  - [[concepts/ai-search-seo]] (added cross-reference to the new mini-tools content-durability thesis)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: This is a domain-widening ingest, not a domain-deepening one. Every prior source in this wiki covers B2B cold-email/outbound GTM engineering; this podcast covers general growth marketing at a horizontal consumer+enterprise AI company — launches, video, org design, brand, and unit economics, with almost no literal tactical overlap with the cold-email stack. The connective tissue is at the principle level: messaging discipline parallels [[concepts/icp-avatar]], the merged product/growth/marketing role parallels [[concepts/gtm-engineering]]'s automation thesis, and Harries' explicit "paid marketing before PMF is the most expensive early mistake" is a soft tension with this wiki's existing paid-ads sources (Schneider), which assume PMF is already in hand. Given the unusual density of distinct, falsifiable advice in one 45-minute transcript (16 named topics in the full-guide breakdown), this ingest intentionally exceeds the normal 5-15 page target.

---

## [2026-07-08] ingest | Nick Abraham — LinkedIn InMail List Pipeline

- Summary page: [[sources/nickabraham-linkedin-inmail-pipeline]]
- Raw source: renamed to `raw/sources/nickabraham-linkedin-inmail-pipeline.md` (original filename too long for git)
- Pages created:
  - [[sources/nickabraham-linkedin-inmail-pipeline]]
  - [[concepts/linkedin-inmail-pipeline]]
  - [[entities/getleads]]
  - [[entities/netnut]]
- Pages updated:
  - [[entities/nick-abraham]] (added InMail scale: 250K+/month; second source; key claims table expanded)
  - [[entities/apify]] (added second use case: active user filter for InMail; 30-60 day activity check)
  - [[concepts/signal-infrastructure]] (added LinkedIn activity behavioral signal layer; active user filter in send list context)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: LinkedIn gives 50 paid InMail credits/license/month. If the paid balance hits zero, LinkedIn freezes all sends including the free Open Profile tier. At 250K InMails/month, list quality is existential — even 3-5 non-open profiles per day drains the balance in a week. The 5-step pipeline (GetLeads → NetNut open-profile split → Apify active-user filter → AI ICP validation → segment-then-sequence) is the protection layer. The critical nuance: open-profile status is not permanent, so the sequencer must recheck at send time. Sequencer choice is a functional requirement, not a preference. Sales Nav lists run 30-40% open profiles vs. 5-8% for standard databases — a meaningful channel-specific sourcing advantage.

---

## [2026-06-24] ingest | Post by @codyschneider — TAM Mapping Playbook

- Summary page: [[sources/codyschneider-tam-mapping]]
- Raw source: renamed to `raw/sources/codyschneider-tam-mapping.md` (original filename too long for git)
- Pages created:
  - [[sources/codyschneider-tam-mapping]]
  - [[concepts/tam-mapping]]
  - [[entities/leadmagic]]
  - [[entities/prospeo]]
  - [[entities/pdl]]
- Pages updated:
  - [[concepts/signal-infrastructure]] (added "signals need a base map" prerequisite section; signals are noise without TAM)
  - [[concepts/enrichment-waterfall]] (added TAM enrichment context; LeadMagic, Prospeo, PDL named; AI soft-qualifier research track noted)
  - [[concepts/icp-avatar]] (added machine-sortable ICP variables as Step 1 of TAM mapping; vibe vs. variable set distinction)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: TAM is a list, not a number. The 5-step process (ICP variables → universe pull → enrich + qualify → tier → layer signals) produces a living asset that all GTM motion runs on. The critical insight: signal infrastructure only works if signals land on accounts you already wanted — the TAM map is the prerequisite that makes signals actionable. Without it, you're running good intelligence on bad targeting.

---

## [2026-06-16] ingest | Post by @codyschneider — Facebook Ads Andromeda Update

- Summary page: [[sources/codyschneider-andromeda-b2b-facebook]]
- Raw source: `raw/sources/codyschneider-andromeda-b2b-facebook.md` (renamed from long filename)
- Pages created:
  - [[sources/codyschneider-andromeda-b2b-facebook]]
- Pages updated:
  - [[concepts/ai-ugc-ads]] (added Andromeda section: creative IS targeting; packs over single ad; broad targeting works because Andromeda does audience-finding)
  - [[concepts/signal-infrastructure]] (added Andromeda paid ads signal layer: clean pixel + CAPI + real conversion events; same "no garbage in" principle as GTM data warehouse)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: The Andromeda algorithm update is the theoretical foundation for Schneider's entire Facebook ads approach. It explains why broad targeting works (algo does audience-finding from creative signals), why creative volume scales (each creative finds a different buyer cohort), and why clean conversion events are non-negotiable (bad signal corrupts the algorithm's learning). The moat shifted from media-buying tricks to persona definitions + creative volume + data infra — three things the wiki already covers in depth.

---

## [2026-06-16] ingest | Post by @codyschneider — Transcript-Based Personas for Facebook Ads

- Summary page: [[sources/codyschneider-transcript-personas]]
- Raw source: `raw/sources/Cody Schneider on X man the biggest arbitrage right now...md`
- Pages created:
  - [[sources/codyschneider-transcript-personas]]
- Pages updated:
  - [[concepts/icp-avatar]] (added Schneider's 4-part persona definition; persona vs. demographic distinction; transcript mining as primary research; desire→hook, fear→body, belief→agreement ad structure)
  - [[concepts/ai-ugc-ads]] (ranked research sources: transcripts best, Reddit proxy; added persona→script mapping)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: Persona = motivation + desire + fear + belief. Demographic = the room, not the why. Everyone targeting "VP Marketing, 50-200 employees" writes ads to the room and converts at agency average. The transcripts already hold the real language — mine 10, find 3-4 repeating motivations, write to those. The arbitrage closes as more teams adopt LLMs to extract this data.

---

## [2026-06-16] ingest | Post by @codyschneider — Facebook Ads for SaaS 101

- Summary page: [[sources/codyschneider-fb-ads-ugc-playbook]]
- Raw source: `raw/sources/Post by @codyschneider on X 4.md`
- Pages created:
  - [[sources/codyschneider-fb-ads-ugc-playbook]]
  - [[entities/seedance]]
  - [[entities/veo3]]
- Pages updated:
  - [[concepts/ai-ugc-ads]] (added Perplexity+Reddit research step; Business Page Admin targeting; click→conversion campaign phasing; GTM tracking stack; Seedance and Veo3 as HeyGen alternatives)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: The UGC ad creative pipeline now has a complete research-to-publish spec. Perplexity + Reddit exact quotes eliminate the brand-copy problem at the research stage. Campaign structure is click-first (7 days) to identify winners cheaply, then convert — and misfiring pixels are the most common cause of apparent "creative fatigue." Three video generation options now in the wiki: HeyGen, Seedance, Veo3.

---

## [2026-06-16] ingest | Post by @codyschneider — AI Search Is Just SEO

- Summary page: [[sources/codyschneider-ai-search-seo]]
- Raw source: `raw/sources/Post by @codyschneider on X 3.md`
- Pages created:
  - [[sources/codyschneider-ai-search-seo]]
  - [[concepts/ai-search-seo]]
  - [[entities/promptwatch]]
- Pages updated:
  - [[concepts/gtm-agents]] (added SEO agent tactical spec: two-lever system, PromptWatch for citation mapping, Instantly for citation outreach)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: AI search optimization reduces to two levers — rank page 1-3 for bottom-of-funnel comparison keywords, and acquire citations from sources AI search already trusts. PromptWatch identifies which citations dominate a category; priority-stacking by citation frequency determines where to concentrate spend. The SEO agent executes Lever 1 autonomously; Lever 2 maps to the cold outreach agent.

---

## [2026-06-10] ingest | [METHOD] FB Ads Library + Claude = $$$ (BlackHatWorld)

- Summary page: [[sources/theory-fb-ads-library-claude-saas]]
- Raw source: `raw/sources/METHOD FB ads Library + Claude = $$$.md`
- Pages created:
  - [[sources/theory-fb-ads-library-claude-saas]]
  - [[concepts/ad-library-market-validation]]
  - [[entities/lovable]]
  - [[entities/higgsfield]]
- Pages updated:
  - [[concepts/saas-lifecycle]] (added compressed lifecycle section: 8 phases → ~10 days via FB Ads Library + Claude + Lovable)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: Facebook Ads Library ad longevity (1+ week running in premium markets) is a proxy for product-market fit before you've built anything. Claude scores opportunities for SaaS recurring potential, generates a full Lovable-ready spec, and the build takes ~9 days. The author built 3 of 6 portfolio products this way — £2,950 combined MRR. The core filter: recurring operational pain (subscription-worthy) vs. one-off pain (not SaaS).

---

## [2026-06-02] ingest | Post by @codyschneider — Stop Overcomplicating Paid Ads for SaaS

- Summary page: [[sources/codyschneider-paid-ads-playbook]]
- Raw source: `raw/sources/Post by @codyschneider on X 2.md`
- Pages created:
  - [[sources/codyschneider-paid-ads-playbook]]
- Pages updated:
  - [[concepts/gtm-agents]] (added paid ads tactical spec section: Google phrase-match intent + Facebook creative-volume system + CLV measurement framework)
  - [[entities/graphed]] (added paid ads dashboard role; named alongside Looker Studio as the recommended measurement layer)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: Schneider's paid ads playbook reduces to two simple systems — Google for intent capture (bottom-of-funnel phrase match), Facebook for creative volume (10/week, isolate winners). Measurement collapses to one number: $1 in → $5 CLV out. Complexity is the failure mode, not the solution.

---

## [2026-05-22] ingest | Post by @codyschneider — Marketing Agents Per Vertical

- Summary page: [[sources/codyschneider-marketing-agents-per-vertical]]
- Raw source: `raw/sources/Post by @codyschneider on X 1.md`
- Pages created:
  - [[sources/codyschneider-marketing-agents-per-vertical]]
  - [[entities/airbyte]]
  - [[entities/clickhouse]]
- Pages updated:
  - [[concepts/data-warehouse-for-ai]] (Airbyte + ClickHouse named as the open-source stack; resolves standing open question; 2–3 week setup caveat added)
  - [[concepts/gtm-agents]] (sources frontmatter updated)
  - [[concepts/gtm-engineering]] (agent-per-vertical model added; self-generating skill files loop)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: The GTM agent model scales as one agent per marketing channel, each with SQL access to a shared Airbyte + ClickHouse warehouse. The differentiating step: agents research best practices and write their own skill files — turning schema-governed behavior into a self-compounding loop. The data warehouse (not the LLM) is the moat.

---

## [2026-04-15] ingest | Post by @codyschneider — Generate + Verify Email Agent

- Summary page: [[sources/codyschneider-email-generation-agent]]
- Raw source: `raw/sources/Post by @codyschneider on X.md`
- Pages created:
  - [[sources/codyschneider-email-generation-agent]]
- Pages updated:
  - [[concepts/enrichment-waterfall]] (added generate + verify as zero-cost alternative; catch-all domain caveat 30–40%)
  - [[entities/graphed]] (noted dual role: analytics layer + GTM agent builder)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: Email addresses are guessable from LinkedIn profiles + domain patterns. A cheap existence-check API + deliverability validator makes this nearly free. Critical caveat: 30–40% of business domains are catch-alls — any pattern returns "valid," making the technique unreliable for that segment.

---

## [2026-04-15] ingest | Thread by @NickAbraham12 — Claude Code for Campaign List Management

- Summary page: [[sources/nickabraham-claude-code-campaign-lists]]
- Raw source: `raw/sources/Thread by @NickAbraham12.md`
- Pages created:
  - [[sources/nickabraham-claude-code-campaign-lists]]
  - [[entities/nick-abraham]]
  - [[entities/discolike]]
- Pages updated:
  - [[concepts/gtm-engineering]] (added Nick Abraham's live operational workflow as the most concrete Claude Code + MCP use case in the wiki)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: At 15+ concurrent campaigns, list management becomes the bottleneck — not copy or strategy. Claude Code + MCP handles org hierarchy resolution (ICP title doesn't exist at smaller companies → Claude finds who holds the role) and industry-specific title patterns autonomously. The ceiling is MCP quality, not LLM capability.

---

## [2026-04-15] ingest | Cold Email Copy Playbook (Anonymous, Notion export)

- Summary page: [[sources/anon-cold-email-copy-playbook]]
- Raw source: `raw/sources/Cold Email Copy Playbook/` (9 markdown files)
- Pages created:
  - [[sources/anon-cold-email-copy-playbook]]
- Pages updated:
  - [[concepts/cold-email-copywriting]] (major update: added 5 psychological triggers, 4-element structure with word counts, subject line open rate data, Friction Test CTA hierarchy, segmentation by ACV, 5-email follow-up sequence with angles, 7 golden rules, diagnostic guide)
  - [[wiki/index.md]], [[wiki/log.md]], [[wiki/overview.md]]
- Key takeaway: 65% of replies come from follow-up emails 2–5 — the first email is the door knock, not the conversation. The Friction Test ranks CTAs by reply rate (Yes/No highest → "Book a call" lowest). Under 80 words is the hard ceiling. Subject lines: question + company name = 38% open rate; 7+ words = 19%.

---

## [2026-04-15] ingest | The Comprehensive Guide to Scalable B2B Cold Email Systems (Anonymous)

- Summary page: [[sources/anon-cold-email-systems-guide]]
- Raw source: `raw/sources/emails.docx`
- Pages created:
  - [[sources/anon-cold-email-systems-guide]]
  - [[concepts/cold-email-infrastructure]]
  - [[concepts/cold-email-copywriting]]
- Pages updated:
  - [[concepts/cold-email-personalization-problem]] (added pre-AI practitioner framing; Spin Tax Rule; infrastructure vs. copy diagnostic separation)
  - [[wiki/index.md]], [[wiki/overview.md]]
- Key takeaway: Cold email is a system with two distinct failure layers — infrastructure (deliverability; 20/day speed limit) and copy (offer specificity; personalization). Conflating them produces wrong diagnoses. The Golden KPI is 1 closed deal per 10,000 prospects. The pay-per-call model removes client risk and aligns incentives at the handoff point (booked meeting, not closed deal).

---

## [2026-04-14] ingest | Email Marketing Squeeze and Scale — Lemlist Case Study (Spicy Lemon)

- Summary page: [[sources/squeezeandscale-lemlist-email-nurturing]]
- Raw source: `raw/sources/Email marketing Squeeze and scale.md`
- Language: French podcast transcript
- Pages created:
  - [[sources/squeezeandscale-lemlist-email-nurturing]]
  - [[concepts/behavioral-email-triggers]]
  - [[entities/customer-io]]
  - [[entities/spicy-lemon]]
- Pages updated:
  - [[entities/lemlist]] (major update: added Lemlist as SaaS case study, not just outreach tool; key stats; internal stack)
  - [[concepts/data-warehouse-for-ai]] (added Lemlist's BigQuery implementation; real-world confirmation of the pattern)
  - [[wiki/index.md]], [[wiki/overview.md]]
- Key takeaway: Timing and relevance beat copy quality. The shift from temporal flows (J+2 after signup) to behavioral triggers (action-based, dynamically routed) produced +800 demos/6 months, +4pts conversion, -40% churn at Lemlist. The highest-ROI single intervention: pre-filling booking forms with known data → +120–130% demos from the same lead volume, with zero dev work.

---

## [2026-04-14] ingest | SalesCaptain's LinkedIn Outbound Playbook 2026 (Bill Stathopoulos)

- Summary page: [[sources/salescaptain-linkedin-outbound-playbook]]
- Raw source: `raw/sources/SalesCaptain's LinkedIn Outbound Playbook 2026.pdf`
- Pages created:
  - [[sources/salescaptain-linkedin-outbound-playbook]]
  - [[entities/heyreach]]
  - [[entities/lemlist]]
  - [[entities/trigify]]
  - [[entities/teamfluence]]
  - [[entities/fibbler]]
  - [[entities/rb2b]]
  - [[entities/findymail]]
  - [[entities/zerobounce]]
  - [[concepts/content-outbound-flywheel]]
- Pages updated:
  - [[concepts/signal-infrastructure]] (added 7 LinkedIn-specific workflows, LinkedIn signal types, critical signal rule)
  - [[concepts/enrichment-waterfall]] (added specific coverage numbers: 50–60% → 85%+, ZeroBounce validation step)
  - [[entities/bill-stathopoulos]] (added LinkedIn playbook claims)
  - [[entities/salescaptain]] (added stats: $1M+ pipeline, 22+ meetings/month, 79% ICP fit)
  - [[wiki/index.md]], [[wiki/overview.md]]
- Key takeaway: LinkedIn's real power is content + outbound as a flywheel, not either alone. 8 data-backed DM principles from 120K+ DMs. The critical signal rule: use signals for targeting, never in the message copy.

---

## [2026-04-14] ingest | SalesCaptain's Claude Code for GTM Playbook (Bill Stathopoulos)

- Summary page: [[sources/salescaptain-claude-code-gtm-playbook]]
- Raw source: `raw/sources/SalesCaptain's Claude Code for GTM playbook.pdf`
- Pages created:
  - [[sources/salescaptain-claude-code-gtm-playbook]]
  - [[entities/bill-stathopoulos]]
  - [[entities/salescaptain]]
  - [[concepts/icp-avatar]]
- Pages updated:
  - [[concepts/gtm-engineering]] (added SalesCaptain's 4 operating modes, 12 playbooks, 8-step pipeline, CLAUDE.md insight)
  - [[concepts/hybrid-ai-model]] (added three-column framework, lead scoring Python rule)
  - [[entities/clay]] (added SalesCaptain's Clay vs. Claude Code by GTM stage, role in 7 LinkedIn workflows)
  - [[wiki/index.md]], [[wiki/overview.md]]
- Key takeaway: CLAUDE.md is the critical enabler — without it Claude is a chatbot, with it it's a GTM engine. The ICP Avatar's 3-level pain hierarchy (surface → operational → identity-level) is the most novel framework in the source: every phrase must come from exact customer quotes.

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
