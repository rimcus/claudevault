---
title: "Overview"
type: overview
tags: [meta, synthesis]
created: 2026-04-14
updated: 2026-08-11
sources: [karpathy-llm-wiki-pattern, codyschneider-gtm-agents, hridoyreh-saas-blueprint, codyschneider-twitter-outreach-pipeline, codyschneider-ai-ugc-ads, alexvacca-gtm-engineering-hire, salescaptain-claude-code-gtm-playbook, salescaptain-linkedin-outbound-playbook, squeezeandscale-lemlist-email-nurturing, anon-cold-email-systems-guide, anon-cold-email-copy-playbook, nickabraham-claude-code-campaign-lists, codyschneider-email-generation-agent, codyschneider-marketing-agents-per-vertical, lukeharries-elevenlabs-growth-playbook, codyschneider-ai-media-company-playbook, maximechampoux-well-ai-native-engineering, codyschneider-ad-library-gap-analysis, codyschneider-seo-for-saas-101, codyschneider-ai-citation-loop, outboundsquad-armandfarrokh-sdr-playbook, codyschneider-two-agents-podcast]
---

# Overview

*The current synthesis of everything in this knowledge base. Updated on every significant ingest.*

## What This Wiki Is

This vault is a personal knowledge base built on [[Andrej Karpathy]]'s [[LLM-Maintained Wiki]] pattern. The core idea: instead of uploading documents to a RAG system that re-derives answers from scratch each time, an LLM incrementally builds and maintains a structured wiki — a compounding artifact where every source added enriches all the existing pages.

**Domain:** AI-powered growth and AI-native building, from three angles that now sit side by side, plus a returning human-operator baseline. The original and still-dominant angle is B2B GTM — the intersection of LLM methodology, autonomous GTM pipelines, and LinkedIn/cold-email outbound systems, useful to anyone scaling a B2B SaaS business on Claude Code and signal-triggered outbound. The [[sources/lukeharries-elevenlabs-growth-playbook|2026-07-15 ingest]] added a second angle: general growth marketing (launches, video, org design, brand, unit economics) at a horizontal consumer+enterprise AI company. The [[sources/maximechampoux-well-ai-native-engineering|2026-07-22 ingest]] added a third: AI-native software engineering process itself — what actually happens inside an engineering org's day-to-day practice once AI coding capability crosses a threshold. The [[sources/outboundsquad-armandfarrokh-sdr-playbook|2026-08-10 ingest]] returns to the original B2B outbound core, but from a human SDR-organization-building angle almost entirely independent of AI tooling — a useful before-picture against which to read the wiki's increasingly AI-native sources. See "A Second Domain Layer," "A Third Domain Layer," and "The Human-Operator Baseline" below for how these connect.

## Current State of Knowledge

**Sources ingested:** 30
**Wiki pages:** 163
**Last activity:** 2026-08-11

## The Emerging Synthesis

Twenty-one sources now form a coherent, layered picture of AI-powered GTM:

1. **[[sources/karpathy-llm-wiki-pattern|Karpathy]]** provides the methodology: LLMs should maintain persistent, compounding knowledge structures rather than re-deriving answers from scratch. This vault is the instantiation.

2. **[[sources/codyschneider-gtm-agents|Schneider]]** applies the same insight to business operations: GTM work can be fully delegated to autonomous [[GTM Agents]] that run always-on. The minimum viable stack is [[Hermes Agent]] + [[Hetzner]] + [[OpenRouter]] + a data warehouse.

3. **[[sources/hridoyreh-saas-blueprint|Hridoy Rehman]]** provides the map: a [[SaaS Lifecycle]] blueprint with 16 phases and ~85 sub-disciplines — showing what's automated vs. what isn't.

4. **[[sources/codyschneider-twitter-outreach-pipeline|Schneider Thread 2]]** introduces the "inbound content outbound cold" strategy and surfaces the [[Cold Email Personalization Problem]].

5. **[[sources/codyschneider-ai-ugc-ads|Schneider Thread 3]]** adds the AI UGC ad pipeline: Reddit pain points → Claude scripts → HeyGen video → FB Ads → CLV-optimized [[Growth Loop]].

6. **[[sources/alexvacca-gtm-engineering-hire|Alex Vacca / ColdIQ]]** provides the empirical layer: 400+ B2B companies, 23M+ cold emails. Validates the hybrid model, names the signal infrastructure layer as the durable differentiator.

7. **[[sources/salescaptain-claude-code-gtm-playbook|SalesCaptain Claude Code Playbook]]** provides the implementation layer: how non-technical GTM teams use Claude Code as a GTM engine. The critical enabler is CLAUDE.md — without it, Claude is a chatbot; with it, it's a business-aware workflow runner at $50–150/month.

8. **[[sources/salescaptain-linkedin-outbound-playbook|SalesCaptain LinkedIn Playbook]]** closes the loop on channel strategy: LinkedIn requires content + outbound working as a [[Content Outbound Flywheel]]. Data-backed across 120,000+ DMs. 7 signal-triggered workflows. 79% ICP fit on inbound.

9. **[[sources/squeezeandscale-lemlist-email-nurturing|Squeeze and Scale — Lemlist]]** (French podcast) extends the wiki into the **retention and lifecycle layer**: the shift from temporal email flows to [[Behavioral Email Triggers]] — using product events as triggers and LLMs for personalization. Validated at 7M emails/year scale: +800 demos, +4pts conversion, -40% churn. Confirms that the same signal-infrastructure architecture applies internally (product behavior) as externally (GTM signals). The most impactful single fix: pre-fill booking forms with known data → +120% demos at zero dev cost.

10. **[[sources/anon-cold-email-systems-guide|Cold Email Systems Guide]]** (anonymous practitioner) provides the **infrastructure and pricing layer** for cold email: the 20-emails/day speed limit, domain/inbox architecture, pay-per-call pricing, and the Meat/Potatoes/Toppings copywriting framework. Critically, it separates two failure modes that most sources conflate — infrastructure failures (deliverability) vs. copy failures (offer/personalization) — each with distinct diagnostics and fixes.

11. **[[sources/anon-cold-email-copy-playbook|Cold Email Copy Playbook]]** (anonymous Notion export) deepens the copy layer: 5 psychological triggers, 4-element structure (≤80 words), subject line data (38% open rate: question + company name), Friction Test CTAs, 9 templates, ACV-based segmentation, 5-email follow-up sequence (65% of replies from emails 2–5), and 7 golden rules. Confirms and extends the systems guide's copy framework.

12. **[[sources/nickabraham-claude-code-campaign-lists|Nick Abraham thread]]** validates Claude Code + MCP as a live operational tool at scale: 15+ concurrent campaigns, list management from 5hrs → 2hrs/week, org hierarchy intelligence, and the key architectural insight: *the MCP quality is the ceiling on Claude Code capability, not the LLM.*

13. **[[sources/codyschneider-email-generation-agent|Schneider — Email Generation Agent]]** adds a zero-cost enrichment path: generate email patterns from LinkedIn + mailtester.ninja existence check + MillionVerifier validation. Critical caveat: unreliable on 30–40% of domains that are catch-alls.

22. **[[sources/nickabraham-linkedin-inmail-pipeline|Abraham — LinkedIn InMail List Pipeline]]** (July 2026) is the most operationally specific source in the wiki. At 250,000+ InMails/month, [[Nick Abraham]] documents the failure mode that most teams hit silently: LinkedIn gives 50 paid InMail credits per Sales Navigator license per month. If paid credits hit zero, LinkedIn freezes all sending — including the 400–800 free sends to Open Profiles. Three to five non-open profiles per day in the send queue burns the balance within a week. The 5-step pipeline built to prevent this: (1) pull raw list via [[GetLeads]] (LinkedIn URL only — no email or domain required), (2) run every URL through [[NetNut]] API to flag open-profile status and split into two buckets, (3) filter for contacts active on LinkedIn in the last 30–60 days via [[Apify]] (higher response rates across all channels), (4) validate ICP fit via AI qualification agent (industry, profile, role), (5) segment open vs. non-open before any sequencer load. The non-obvious insight: open-profile status is not permanent. A contact enriched as "open" today may flip to "closed" before the sequencer sends — so sequencer choice for InMail is a functional requirement: it must recheck open status at send time, not just at list-load. Sales Navigator lists run 30–40% open-profile density vs. 5–8% for standard database pulls, because Sales Nav sorts open profiles to the front of results. The pipeline logic connects to the wiki's signal infrastructure and TAM mapping frameworks: the active-user filter is behavioral signal applied at the contact level; the ICP validation step applies the machine-sortable ICP principle before committing scarce credits.

21. **[[sources/codyschneider-tam-mapping|Schneider — TAM Mapping Playbook]]** (June 2026) is the foundational infrastructure post — the layer that sits beneath all outbound, ads, and signal work. TAM is not a number; it's a named account database (bottoms-up, enriched, tiered) that is the living asset all GTM sits on. The five-step process: (1) ICP in machine-sortable variables, (2) over-pull the universe (Crunchbase, BuiltWith, Apollo), (3) enrich contacts via waterfall (LeadMagic, Prospeo, PDL, Findymail) and qualify soft signals via AI research, (4) tier 1/2/3 on fit, (5) layer live signals on top. The critical insight: **signals are noise without a base map.** Signal infrastructure is only as good as the TAM map it fires onto. This post retroactively explains why most teams running intent signals get poor results — they're chasing triggers without first controlling the target account universe. Introduces TAM Mapping as a new concept and LeadMagic, Prospeo, PDL as new entities.

20. **[[sources/codyschneider-andromeda-b2b-facebook|Schneider — Andromeda & B2B Facebook Ads]]** (June 2026) is the theoretical capstone for the entire Schneider paid ads stack. Meta's Andromeda algorithm killed audience-first targeting — the algo now reads creative + landing page, predicts converters from behavioral signals, and finds them. For B2B, this removes the channel's historical limitation (can't target niche professional audiences) and turns creative into the targeting mechanism. The two inputs that now matter: (1) creative packs — multiple angles to reach multiple buyer cohorts simultaneously, and (2) clean signal data — pixel + Conversion API + real conversion events (signup, payment). The moat shifted from media-buying tricks to persona definitions + creative volume + data infrastructure. This post explains *why* the other Schneider Facebook posts recommend what they recommend.

19. **[[sources/codyschneider-transcript-personas|Schneider — Transcript-Based Personas]]** (June 2026) provides the creative input layer that the UGC ad pipeline was missing: how to define personas before writing a script. The core reframe: a persona is motivation + desire + fear + belief — not a demographic. Demographics tell you who's in the room; they never explain why anyone acts. The data already lives in sales call transcripts. Mine 10, extract exact language, find 3–4 repeating motivations. Those become your creative directions, with desire in the hook, fear in the body, and the pre-existing belief acknowledged before reframing. This post connects the [[ICP Avatar]] framework (developed for outbound copy by SalesCaptain) to the Facebook ads creative layer — confirming that the same principles govern ad copy and cold email copy.

18. **[[sources/codyschneider-fb-ads-ugc-playbook|Schneider — Facebook Ads for SaaS 101]]** (June 2026) provides the granular execution detail missing from the earlier paid ads and UGC ad posts. The novel elements: Perplexity as a Reddit pain-point research tool (search "pain points X person has for Y thing my Z product solves reddit" → extract exact quotes → Claude scripts), Business Page Admin targeting as a B2B proxy on Facebook, and the click-first→conversion-campaign phasing (7 days cheap signal, then commit spend). Also adds [[Seedance]] and [[Veo3]] as alternatives to [[HeyGen]] for video generation. The Facebook Ads agent now has a complete tactical spec across three posts.

17. **[[sources/codyschneider-ai-search-seo|Schneider — AI Search Is Just SEO]]** (June 2026) closes the loop on the SEO agent's tactical spec. The reframe: AI search is not a new discipline — two levers only. Lever 1: rank page 1–3 for comparison keywords ("best X for Y," "X alternative," etc.) → AI search pulls traffic from those pages. Lever 2: acquire citations from sources AI platforms already trust, mapped via [[PromptWatch]] and acquired via cold email ([[Instantly]]). Priority-stack citations by frequency — a small number of sources dominate citation share in each category. Introduces [[AI Search SEO]] as a concept and [[PromptWatch]] as a new entity.

16. **[[sources/theory-fb-ads-library-claude-saas|FB Ads Library + Claude Method]]** (BlackHatWorld, May 2026) is the first source in this wiki to address the **pre-GTM build phase** — specifically, how to validate demand before building. The technique uses Facebook Ads Library ad longevity as a proxy for product-market fit, Claude to score for SaaS recurring potential and generate a full Lovable-ready spec, and [[Lovable]] (AI app builder) to produce 75–80% of the MVP in one session. Total cycle: ~10 days idea-to-paying-customers. Results: £2,950 combined MRR across 6 products. Introduces two new entities ([[Lovable]], [[Higgsfield]]) and a new pattern concept ([[Ad Library Market Validation]]) that extends the wiki upstream into the product discovery and validation phases of the [[SaaS Lifecycle]].

15. **[[sources/codyschneider-paid-ads-playbook|Schneider — Paid Ads Playbook]]** (June 2026) is the most tactical source yet: a prescriptive two-platform system (Google: bottom-of-funnel phrase match; Facebook: 10 creatives/week + winner isolation) with a one-number measurement test ($1 in → $5 CLV out). Provides the tactical spec that the Google Ads and Facebook Ads agents in the [[GTM Agents]] blueprint actually run. The core principle: simplicity beats cleverness in SaaS paid ads.

14. **[[sources/codyschneider-marketing-agents-per-vertical|Schneider — Agents Per Vertical]]** (May 2026) refines the GTM agents model: **one agent per channel**, each with SQL access to a shared [[Airbyte]] + [[ClickHouse]] warehouse. The breakthrough step: agents research best practices and **write their own skill files** — turning schema-governed behavior into a self-compounding loop. Confirms the data warehouse (not the LLM) is the durable moat. Also reveals [[Graphed]] has pivoted toward a service model (forward-deployed engineers in 5 business days).

### The Key Synthesis

All eight sources converge on the same underlying architecture:

```
Signal fires (LinkedIn engagement, site visit, hiring trigger, funding event)
    → Signal platform (Trigify / RB2B / Fibbler / Common Room)
    → Enrichment and qualification (Clay + waterfall)
    → Copy generation (Claude Code + ICP Avatar playbook)
    → Outreach execution (HeyReach / Lemlist / Instantly)
    → Performance analysis → feeds next cycle
```

The variation across sources is in which layer each one emphasizes:
- **Schneider:** the agent runtime layer
- **Vacca:** the signal and enrichment layer
- **Stathopoulos:** the Claude Code workflow and LinkedIn signal layer

### The Three Durable Differentiators (Vacca, confirmed by SalesCaptain)

As tooling commoditizes, the moat narrows to three things:

1. **[[Signal Infrastructure]]** — the upstream data layer most teams skip. LinkedIn-specific: Trigify, Fibbler, Teamfluence, RB2B. Each captures different buyer intent signals.
2. **[[ICP Avatar]]** — the 3-level pain hierarchy (surface → operational → identity-level). Every phrase from exact customer quotes. Generic ICPs produce generic outreach that AI amplifies into noise.
3. **[[Hybrid AI Model]]** — AI on volume, humans on judgment. SalesCaptain's three-column framework (Automate / Keep Manual / Hybrid) is the most actionable implementation of this principle.

### New: The CLAUDE.md Insight

[[Bill Stathopoulos]] contributes a key insight that directly extends [[Schema-Governed LLM Behavior]]: the CLAUDE.md file is what transforms Claude Code from a capable tool into a business-specific GTM engine. The 12 playbooks (ICP Profile, Brand Voice, Lead Scorer, Outreach Writer, etc.) are the persistent memory that makes the system compound over time — consistent with Karpathy's core methodology, applied to revenue operations.

### What the Stack Actually Covers (vs. the Full SaaS Blueprint)

| SaaS Phase | Coverage | Source |
|------------|----------|--------|
| Acquisition (SEO) | Landing pages (3/day), blog pipeline | Schneider |
| Acquisition (LinkedIn Outbound) | 7 signal-triggered workflows, content flywheel | SalesCaptain |
| Acquisition (Twitter Outreach) | Engager → enrich → cold email | Schneider |
| Acquisition (Paid) | Google + Facebook Ads optimization | Schneider |
| Acquisition (Cold Email) | Infrastructure (domains/inboxes/warmup), copy, pricing system | Cold Email Systems Guide |
| Acquisition (Outbound) | Signal-triggered enrichment → sequencing | Vacca |
| Activation | Behavioral email flows triggered on product actions | Squeeze and Scale / Lemlist |
| Retention | Churn prevention flows (behavioral triggers + multi-channel) | Squeeze and Scale / Lemlist |
| Expansion | Post-purchase upsell timing, credit-triggered offers | Squeeze and Scale / Lemlist |
| Advocacy | G2/Capterra review collection via behavioral triggers | Squeeze and Scale / Lemlist |
| Retention (old) | Email nurture optimization | Schneider |
| Analytics / CRM | HubSpot enrichment, PostHog + Stripe tracking | Schneider + Vacca |
| **Uncovered** | Idea, Validation, Planning, Design, Dev, Infrastructure, Launch, Distribution, Conversion, Revenue, Growth, Scaling | — |

The GTM layer is increasingly automatable. The product layer remains human.

## A Second Domain Layer: General Growth Marketing

**23. [[sources/lukeharries-elevenlabs-growth-playbook|Luke Harries — ElevenLabs Growth Playbook]]** (July 2026) is the wiki's first source outside the B2B cold-email/outbound-GTM core. [[entities/luke-harries|Luke Harries]] (Head of Growth, [[entities/elevenlabs|ElevenLabs]]) covers launches, video strategy, org design, brand, and unit economics for a horizontal consumer+enterprise AI company — almost none of it literal cold-email or signal-infrastructure tactics. Nine new concepts capture it: [[concepts/launch-playbook|tiered launches]] (200K–700K views per Tier 1 launch), [[concepts/growth-video-strategy|three video formats]] governed by a first-30-seconds rule, [[concepts/sharded-growth-teams|sharded team structure]] for horizontal multi-product companies, [[concepts/growth-hiring-order|a fixed growth-hiring sequence]], [[concepts/cac-payback-period|CAC-to-payback-period]] as the operating ratio (not CAC:LTV), [[concepts/product-engineers-no-pms|a no-PM, product-engineer-owned roadmap]] model, [[concepts/counter-positioning|counter-positioning]] as a brand-strategy pattern, [[concepts/seo-mini-tools|durable SEO mini-tools]] that survive the AI-search shift, and [[concepts/founder-brand-strategy|founder-brand channel-fit]] guidance.

**Why this belongs in the same wiki despite the domain shift**: the connective tissue is principle-level, not tactical. Harries' messaging-first launch discipline parallels [[concepts/icp-avatar]]'s insistence on exact customer language. His no-PM, engineers-own-the-roadmap thesis parallels [[concepts/gtm-engineering]]'s broader claim that AI collapses traditionally separate roles into merged, code-adjacent ones. And his stated rule — never run paid marketing before PMF — is a **soft tension**, not a contradiction, with the wiki's existing Schneider paid-ads sources, which assume PMF is already established before their playbooks start. Read together: Schneider's paid-ads and UGC-ad sources answer "how do you scale paid spend once PMF exists," and Harries answers "what do you do before that, and what does the org around it look like."

**24. [[sources/codyschneider-ai-media-company-playbook|Schneider — AI Media Company Playbook]]** (July 2026) returns to the core B2B/GTM-agents domain but widens its unit of production from single-function agents to entire agent-run *media properties*. The concept it introduces, [[concepts/ai-media-company-playbook]], reframes prior wiki tactics — SEO, content, social — as pieces of a business running its own owned-media operation as an ad-placement funnel rather than a marketing department producing occasional assets. Three tactics: a scraped-dataset [[concepts/directory-website-seo-play|directory website]] (Hermes agent scrape → Claude Code one-shot build → Vercel → Search Console, refreshed monthly), a [[concepts/podcast-newsletter-growth-loop|podcast + newsletter]] loop (interview research → agent-scripted monologue → ElevenLabs TTS → Transistor.fm → newsletter as the ad-monetized asset, to a claimed 20K list in 6 months), and a [[concepts/tiktok-reel-farm|TikTok reel farm]] (DoubleSpeed AI cloud accounts → Nano Banana viral-format slideshows, ~300K aggregate impressions at ~$3 CPM across a 10-account cohort). All figures are single-source claims with no methodology given — treat as directional, not verified. Notably, this is the first wiki source to use [[entities/elevenlabs|ElevenLabs]] as a third-party production tool rather than as the company profiled in the Harries growth playbook — the two ElevenLabs mentions in this wiki are now genuinely unrelated contexts (org/growth strategy vs. TTS-as-a-tool).

**26. [[sources/codyschneider-ad-library-gap-analysis|Schneider — Competitor Ad Library Gap Analysis]]** (July 2026) stays within the core GTM-agents domain and sharpens the paid-ads pipeline further: instead of researching customer pain first ([[concepts/ai-ugc-ads]]'s Reddit/transcript sources), it researches the *competitive field* first — scrape every competitor's Facebook Ads Library creative via Apify, have Gemini describe each ad's angle/promise/outcome, have Claude find the gap in how the category talks about itself, then validate that gap against real Reddit complaints before generating anything. The new concept, [[concepts/competitor-creative-gap-analysis]], is the wiki's clearest example yet of an agent both *analyzing* performance data (via a Graphed MCP connection into Claude Code) and *executing* the resulting decision directly (calling the Facebook Ads API to kill losers and reallocate budget) with no human step between the two — then the whole loop is deployed to a server to run unattended. Notably the only Schneider source in the wiki with zero supporting metrics; treat the method as directional, unverified by results.

**27. [[sources/codyschneider-seo-for-saas-101|Schneider — SEO for SaaS 101]]** (July 2026) restates the wiki's existing [[concepts/ai-search-seo]] Lever 1 with named tools (Claude Code + an SEO API for keyword discovery, [[entities/serper|Serper]] for page-1 scraping) and one genuinely new step: a recorded founder video, or a Claude-mobile-app interview, folded into the article alongside the competitor research. The new concept, [[concepts/founder-perspective-content-moat]], captures why this matters — a reply to the post (not Schneider himself) names the mechanism precisely: once every SaaS company runs the same mechanical playbook, the ranked article becomes commodity, and the founder's own perspective is the one input an LLM can't synthesize from the other ranking pages. This connects two previously separate wiki threads for the first time — [[concepts/seo-mini-tools]]'s engineering-effort durability argument and [[concepts/founder-brand-strategy]]'s authenticity argument — as a third variant of the same underlying claim, applied to written SEO content specifically. Like the prior Schneider ingest, this post carries zero supporting metrics.

**28. [[sources/codyschneider-ai-citation-loop|Schneider — Half of Winning With AI Search Is Just Writing Content AI Wants to Consume]]** (August 2026) is the most technically detailed Schneider post in the wiki — the first to name specific API endpoints, a literal agent prompt, and structured-data requirements. It proposes a structural alternative to Lever 2 of [[concepts/ai-search-seo]]: instead of buying citation placement via cold email, reverse-engineer the shape of already-cited content ([[entities/promptwatch|PromptWatch]] for the gap, [[entities/dataforseo|DataForSEO]]'s AI Optimization API to size it, [[entities/codex|Codex]] to analyze top-cited URL structure) and mechanically rewrite content to match — because, per the post's central claim, "models retrieve chunks, not pages." The new concept, [[concepts/citation-shape-engineering]], captures the six named structural features (40-word front-loaded answers, literal-question H2s, named-competitor comparison tables, number+date co-location, 200–400 word standalone sections, FAQPage + Article schema). Notably, this post sits in unreconciled tension with [[concepts/founder-perspective-content-moat]] — the prior Schneider ingest, roughly ten days earlier — which argued personal, un-synthesizable perspective is the durable moat once mechanical SEO steps commoditize; this post describes a purely mechanical, agent-run pipeline with no perspective step at all, and neither post acknowledges the other. As with the two prior Schneider ingests, no results/before-after data are given — the method is asserted, not demonstrated.

## A Third Domain Layer: AI-Native Software Engineering

**25. [[sources/maximechampoux-well-ai-native-engineering|Maxime Champoux — Well, SaaS Connection podcast]]** (July 2026) opens a third domain layer distinct from both the cold-email/GTM-agent core and the general growth-marketing layer: **AI-native software engineering process itself**. [[entities/maxime-champoux|Champoux]] (ex-Head of Products at [[entities/qonto|Qonto]], now CEO of [[entities/well|Well]]) documents his prior team's Toyota-Production-System-inspired engineering culture ([[concepts/toyota-production-system-for-software]]) and then, in far more granular and dated detail, his current 12-person team's transition from ~7 to 100+ shipped features/month between November 2025 and the recording — including the part almost no public AI-coding account includes: a specific, diagnosed quality plateau and its fix. Six new concepts capture it: [[concepts/ai-native-engineering-team|the "everyone codes" transition]] (bounded permissions + full team buy-in as the two required conditions), [[concepts/marginal-gains-1-percent|daily 1% tooling gains]] (borrowed directly from Team Sky cycling), [[concepts/design-code-inversion|the Figma/code source-of-truth inversion]], [[concepts/agent-specialization-context-window|agent specialization by context window]] (the plateau-breaking fix: 8 named, stable, domain-specialized agents plus an orchestrator, triggered once task material exceeds what a generic agent's context window can responsibly hold), [[concepts/roadmap-abstraction-shift|the reshaped Double Diamond]] (concept-level vision + black-box feature briefs once detailed specs no longer make sense), and [[concepts/business-context-graph|the business context graph]] (Well's own product: a unified SMB data model, MCP-first and demand-driven).

**Why this belongs in the same wiki despite yet another domain shift**: the connective tissue here is unusually direct, not just principle-level. [[concepts/agent-specialization-context-window]] — named, stable, context-bounded agents orchestrated by an intent-reading dispatcher, each documenting its own domain knowledge as reusable skills — is functionally the same pattern this wiki already tracks in two other places: [[concepts/schema-governed-llm-behavior]] (CLAUDE.md as persistent, co-evolved configuration) and [[concepts/gtm-agents]]' "agents write their own skill files" loop from [[sources/codyschneider-marketing-agents-per-vertical]]. Three unrelated sources, three different domains (wiki maintenance, GTM automation, core engineering), converging on the same architecture is stronger evidence than any one of them alone. Separately, [[concepts/roadmap-abstraction-shift]] and [[concepts/product-engineers-no-pms]] describe the same underlying trend (PM work compressing as AI coding capability rises) from two different companies and mechanisms — Champoux's PM role moves up in abstraction rather than disappearing outright, where Harries' ElevenLabs eliminates the PM function entirely; read together they bound a range of what "AI collapses the PM role" can mean in practice, rather than describing one settled outcome. [[concepts/business-context-graph]] is also a direct SMB-scale variant of this wiki's existing [[concepts/data-warehouse-for-ai]] thesis.

## The Human-Operator Baseline: SDR Leadership Without AI

**29. [[sources/outboundsquad-armandfarrokh-sdr-playbook|Armand Farrokh — Outbound Squad podcast]]** (August 2026) is the wiki's first source on human SDR organization-building specifically, and the first major source since the original outbound-core ingests that isn't primarily about AI tooling. [[entities/armand-farrokh|Farrokh]] (co-founder of [[entities/30mpc|30MPC]]; former SDR leader at [[entities/carta|Carta]]; former Head/VP of Sales at [[entities/pave|Pave]], $0→$13M ARR) documents a complete, sequenced playbook: [[concepts/sdr-org-turnaround-playbook|a 3-week turnaround formula]] ("Flip 2, Fire 2, Hire 2"), [[concepts/sdr-hiring-signal|a hiring process built around the finding that prior SDR experience is a weak predictor of success]], [[concepts/sdr-culture-building|daily culture mechanics]] (a synchronized "dial blitz" plus real-time public recognition), [[concepts/outbound-targeting-triggers|firmographic-plus-trigger-event targeting]] (a technically ICP-matching account can still be a dead end without a live buying trigger), and three creative pipeline-generation plays beyond cold call/cold email: [[concepts/abm-account-based-pipeline-plays|coordinated ABM]] (synchronized SDR + display ads + physical mail), [[concepts/executive-referral-pipeline|systematized executive/investor referrals]], and [[concepts/event-pipeline-pre-booking|event pre-booking and "floor hunting"]].

**Why this belongs in the same wiki**: two direct convergences with existing concepts, from a completely independent vantage point (one operator's personal hiring/coaching practice, not an agency's aggregate data or a GTM-automation playbook). Farrokh's AI-sales-coach critique — useless for nuanced deal judgment, excellent for deterministic account filtering — is a third independent confirmation of [[concepts/hybrid-ai-model]], joining ColdIQ's aggregate client data and SalesCaptain's three-column framework. And his firmographic-plus-trigger "stale cap table" targeting logic is functionally the pre-automation version of [[concepts/icp-avatar]]'s core claim (generic ICP fit produces generic, poorly-timed outreach) — the same insight, one from AI-copywriting practice and one from a human SDR leader's targeting discipline. Three unrelated sources converging on the same "AI for volume, humans for judgment" split, and two unrelated sources converging on "firmographic fit alone is vibes, not a signal," is stronger evidence than either claim would be alone.

## Back to the AI-Native Core: Two GTM Agents, and an Agent-Design Philosophy

**30. [[sources/codyschneider-two-agents-podcast|Schneider — Two GTM Agents (Two Agents Podcast Recap)]]** (August 2026) returns the wiki to its AI-native core after the Farrokh human-operator detour, with the wiki's most explicit statement yet of how Schneider actually thinks agents should be built: [[concepts/agent-architecture-principles]] — an agent is code plus a thinking loop plus a live data stream, deterministic CPU work should never burn tokens, most agent frameworks are bloat for problems that are actually finite, and the design target is a human's real existing process, not an idealized autonomous system. The post itself covers two systems: an evolved, more-automated version of the original April cold-outbound pipeline ([[sources/codyschneider-gtm-agents]]) — now sourced from the LinkedIn For You feed and 10–20 tracked category outliers rather than search, enriched through an [[entities/origami|Origami]]-aggregated waterfall, and closed by an inbox agent with direct calendar access to verify real bookings — and a genuinely new second system, [[concepts/organic-content-agent-loop]], which mines LinkedIn content from internal conversations (sales calls, Slack, Notion, [[entities/gong|Gong]]) instead of prompting an LLM to write from scratch, scheduled across accounts by [[entities/ordinal|Ordinal]] with a live analytics feedback loop.

**Why this belongs in the same wiki, and why it's worth flagging rather than filing quietly**: the organic-content system is a direct structural cousin of [[concepts/founder-perspective-content-moat]] — both claim that valuable content already exists in unstructured, real human material and needs extraction rather than generation, one in SEO articles, one in LinkedIn posts. But the agent-design philosophy sits in real, unreconciled tension with Schneider's own prior recommendation: [[sources/codyschneider-gtm-agents]] (April 2026) names [[entities/hermes-agent|Hermes Agent]] as the recommended runtime framework; this post says agent frameworks are usually bloat. Neither post references the other. This is now the *third* internal contradiction logged against a single author in this wiki — alongside the founder-perspective/citation-shape-engineering tension already on record — worth noting as a pattern in how Schneider's own positions evolve (or simply drift) across a five-month span, rather than treating each post as a standalone, permanently-valid playbook.

## Open Questions / Gaps

- ~~What open-source data warehouse is recommended for Schneider's stack?~~ **Resolved:** [[Airbyte]] + [[ClickHouse]] (named in [[sources/codyschneider-marketing-agents-per-vertical]]). Community caveat: 2–3 week setup minimum for clean data.
- How do GTM agents handle errors or bad decisions? No source addresses agent failure modes or human review checkpoints.
- What covers the Distribution phase? Current stack handles Acquisition but not SaaS Marketplaces, Directories, or Partnerships.
- At what wiki scale should [[qmd]] be introduced?
- Is there a source that addresses GTM Engineering for enterprise sales (complex cycles, relationship layer)?
- SalesCaptain claims 22+ meetings/month from LinkedIn. What is the team size and sequence volume behind that number? [unanswered]
- The Lemlist case study is a French podcast transcript — some nuance may be lost in the transcript-to-wiki translation. Key numbers (800 demos, -40% churn) appear reliable but no written source exists to cross-reference.
- What automation tool does Lemlist use for the multi-channel churn flow (LinkedIn message)? Nicolas mentions "on utilise la liste" — implying Lemlist itself sends the LinkedIn message, which is a nice dogfooding detail but not fully explained.

## See Also

- [[sources/codyschneider-two-agents-podcast]] — two agent systems: evolved cold-outbound pipeline + new organic-content agent
- [[concepts/agent-architecture-principles]] — code + thinking loop + data stream; frameworks as bloat; in tension with the Hermes Agent recommendation
- [[concepts/organic-content-agent-loop]] — mine content from internal conversations; Ordinal scheduling + analytics feedback
- [[sources/outboundsquad-armandfarrokh-sdr-playbook]] — human SDR-organization-building baseline: turnaround, hiring, culture, targeting, creative pipeline plays
- [[concepts/hybrid-ai-model]] — third independent confirmation via Farrokh's AI-sales-coach critique
- [[concepts/icp-avatar]] — pre-AI human-SDR parallel via firmographics-plus-triggers targeting
- [[sources/maximechampoux-well-ai-native-engineering]] — AI-native engineering process layer: Toyota Production System culture, the 7→100+ features/month transition, agent specialization by context window
- [[concepts/agent-specialization-context-window]] — the plateau-breaking fix; converges with schema-governed-llm-behavior and gtm-agents' self-generating skill files
- [[concepts/business-context-graph]] — SMB-scale variant of data-warehouse-for-ai
- [[sources/codyschneider-ad-library-gap-analysis]] — competitor ad creative gap analysis; autonomous analyze-and-execute optimization loop
- [[sources/codyschneider-seo-for-saas-101]] — named-tool SEO Lever 1 spec; founder-perspective content as the durability layer
- [[sources/codyschneider-ai-citation-loop]] — structural citation-acquisition alternative to Lever 2; "models retrieve chunks, not pages"; in tension with the founder-perspective post
- [[sources/codyschneider-ai-media-company-playbook]] — agent-run owned-media properties (directory site, podcast + newsletter, TikTok reel farm) as ad-placement funnels
- [[sources/lukeharries-elevenlabs-growth-playbook]] — general growth-marketing layer: launches, video, org design, CAC:payback, no-PM model
- [[concepts/launch-playbook]] — tiered launch system
- [[concepts/sharded-growth-teams]] — horizontal multi-product growth org design
- [[concepts/cac-payback-period]] — CAC:payback over CAC:LTV; enterprise SQL North Star
- [[sources/karpathy-llm-wiki-pattern]] — founding methodology
- [[sources/codyschneider-gtm-agents]] — GTM agent pipelines
- [[sources/alexvacca-gtm-engineering-hire]] — empirical validation + role definition
- [[sources/salescaptain-claude-code-gtm-playbook]] — Claude Code implementation layer
- [[sources/salescaptain-linkedin-outbound-playbook]] — LinkedIn signal + flywheel
- [[sources/squeezeandscale-lemlist-email-nurturing]] — lifecycle email / retention layer
- [[sources/nickabraham-claude-code-campaign-lists]] — live MCP workflow: Claude Code for campaign list management at scale
- [[sources/nickabraham-linkedin-inmail-pipeline]] — LinkedIn InMail list pipeline at 250K+/month; credit mechanics; open-profile segmentation; sequencer requirements
- [[sources/codyschneider-marketing-agents-per-vertical]] — agent-per-vertical model; Airbyte + ClickHouse; self-generating skill files
- [[GTM Engineering]] — the synthesized concept
- [[Signal Infrastructure]] — the key differentiating layer
- [[Behavioral Email Triggers]] — the internal/product signal equivalent of GTM signal infrastructure
- [[Cold Email Infrastructure]] — the technical plumbing layer; domain/inbox/speed-limit architecture
- [[Cold Email Copywriting]] — Meat/Potatoes/Toppings; 4-element structure (≤80 words); Friction Test CTAs; 5-email follow-up sequence; ACV-based segmentation; 7 golden rules
- [[Content Outbound Flywheel]] — LinkedIn-specific strategic system
- [[ICP Avatar]] — the upstream framework for all copy quality
- [[LLM-Maintained Wiki]] — the core methodology concept
