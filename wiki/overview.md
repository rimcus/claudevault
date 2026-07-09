---
title: "Overview"
type: overview
tags: [meta, synthesis]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern, codyschneider-gtm-agents, hridoyreh-saas-blueprint, codyschneider-twitter-outreach-pipeline, codyschneider-ai-ugc-ads, alexvacca-gtm-engineering-hire, salescaptain-claude-code-gtm-playbook, salescaptain-linkedin-outbound-playbook, squeezeandscale-lemlist-email-nurturing, anon-cold-email-systems-guide, anon-cold-email-copy-playbook, nickabraham-claude-code-campaign-lists, codyschneider-email-generation-agent, codyschneider-marketing-agents-per-vertical]
---

# Overview

*The current synthesis of everything in this knowledge base. Updated on every significant ingest.*

## What This Wiki Is

This vault is a personal knowledge base built on [[Andrej Karpathy]]'s [[LLM-Maintained Wiki]] pattern. The core idea: instead of uploading documents to a RAG system that re-derives answers from scratch each time, an LLM incrementally builds and maintains a structured wiki — a compounding artifact where every source added enriches all the existing pages.

**Domain:** AI-powered B2B GTM — specifically the intersection of LLM methodology, autonomous GTM pipelines, and LinkedIn outbound systems. The wiki is useful to anyone building or scaling a B2B SaaS business using Claude Code and signal-triggered outbound as the primary growth engine.

## Current State of Knowledge

**Sources ingested:** 22
**Wiki pages:** 109
**Last activity:** 2026-07-09

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
