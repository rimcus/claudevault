---
title: "SalesCaptain's Claude Code for GTM Playbook"
type: source
tags: [claude-code, gtm, outbound, playbook, automation, saas]
created: 2026-04-14
updated: 2026-04-14
sources: [salescaptain-claude-code-gtm-playbook]
author: "Bill Stathopoulos"
source_url: ""
source_type: pdf
---

# SalesCaptain's Claude Code for GTM Playbook

**Author:** [[Bill Stathopoulos]], CEO & Co-Founder @ [[SalesCaptain]]
**Date:** 2026
**Scope:** 12 playbooks, 8 pipeline steps, 25 workflows, 5 GTM motions. Tested across 70+ client engagements.

## Core Thesis

Claude Code is not a developer tool — it's a GTM engine that non-technical teams can use in 10 minutes. The word "Code" is a misnomer keeping GTM teams from one of the most powerful productivity tools available. The critical enabler is the **CLAUDE.md file**: without it, Claude is a chatbot; with it, Claude is a GTM engine that knows your business.

## Key Points

- **Total monthly cost:** $50–150/month to run 2–4 campaigns in parallel. Claude subscription ($20) covers AI cost; the variable cost is third-party enrichment APIs. Compare to a full-time SDR at $4K–7K/month.
- **"Without CLAUDE.md → Claude is a chatbot. With CLAUDE.md → Claude is a GTM engine."**
- **The 3-question brief:** Every workflow requires: (1) What are my inputs? (2) What is my output? (3) What does "good" look like? If you can't answer all three, no AI will help.
- **Lead scoring must use Python, not AI.** AI scoring is inconsistent between runs. Python if-then rules produce reproducible results.
- **The ICP Avatar framework** — most ICPs are useless because they describe a company type without explaining *why* someone buys today. The 3-level pain hierarchy solves this.

## The Three Layers

| Layer | What it is |
|-------|-----------|
| **Tools** | Claude's built-in capabilities: read/write files, run Python/JS, search the web, execute commands, manage repos |
| **Playbooks** | Plain-text skill files that teach Claude a specific workflow. Write once, runs every time at the same quality. |
| **Connections** | MCP plug-ins linking Claude to tools (Apollo, HubSpot, Instantly, Slack, etc.) |

"Most teams use only Layer 1. All three together is where the 🚀 happens."

## CLAUDE.md Templates by GTM Motion

| Motion | Key contents | Key signals |
|--------|-------------|-------------|
| Outbound-led | ICP firmographics, tier scoring, copy frameworks, exclusion list | Hiring, funding, tech stack changes |
| PLG | Free-to-paid conversion criteria, usage signals, champion identification | Product usage milestones, feature adoption |
| ABM | Named account list, stakeholder map, multi-thread sequence logic | Executive changes, strategic initiatives |
| Founder-led | Founder voice, warm network prioritisation, referral templates | LinkedIn connections, mutual contacts |
| Agency | Client ICP per project folder, per-client exclusions, per-client copy tone | Separate folder per client, each with own CLAUDE.md |

## The 4 Operating Modes

| Mode | When to use |
|------|-------------|
| **Plan Mode** | Before any new workflow, every time — Claude plans, touches nothing |
| **Auto-Accept Edits** | After reviewing and approving the plan |
| **Auto Mode** | Workflows you've tested and trust completely |
| **Skip Permissions** | Isolated test environments ONLY — never on live data |

Switch between Plan Mode and Auto-Accept with Shift+Tab.

## The 12 Playbooks Every GTM Team Should Build

**Foundation (build first):**
1. **ICP Profile** — full description of ideal customer with signals, pain points, exclusions
2. **Brand Voice** — writing patterns from best emails/posts into a reusable voice guide
3. **Segment-to-Message Mapper** — maps each ICP segment to correct offer angle

**Prospecting:**
4. **Lead Scorer** — Python rules (not AI), zero hallucination risk, outputs Tier 1/2/3
5. **Outreach Writer** — finds timely signal, writes personalised first lines per segment

**Conversion:**
6. **Offer Testing** — runs 3–5 offer angles as mini-campaigns, tracks winning angle per segment
7. **Email Frameworks** — best-performing email structures with routing logic (cold vs. warm)
8. **Objection Handler** — library of 7–10 common objections with proven responses
9. **Copy Stress-Test** — Claude reads your email as the target persona, flags what would get it deleted

**Intelligence:**
10. **Social Proof Matcher** — structured case study library mapped by client type/industry/pain
11. **Meeting Prep** — one-page brief before every call
12. **Call Debrief** — reads transcript, scores BANT, flags red flags, drafts CRM update

## The ICP Avatar: 3-Level Pain Hierarchy

Most ICPs are useless because they describe company types, not buying triggers. The framework:

| Level | What it is | Example (sales ops tool) |
|-------|-----------|--------------------------|
| **Surface pain** | Symptom they describe when asked "what's the problem?" | "Our reporting takes too long" |
| **Operational pain** | Downstream business cost of the surface pain | "We're making quota decisions on stale data" |
| **Identity-level pain** | What this says about them as a professional — the real buy trigger | "I look incompetent in front of the board every quarter" |

**Rule:** Every phrase must come from an exact customer quote. "They struggle with follow-up" is analysis. "Our follow-up is a mess" is a quote.
**Sources:** call transcripts, deal notes, G2/Capterra reviews, lost deal notes, onboarding calls.

## The 8-Step Outbound Campaign Pipeline

| # | Stage | What Claude does |
|---|-------|-----------------|
| 1 | Detect Signals | Monitors job postings, funding, tech changes, LinkedIn engagement, website visitors |
| 2 | Score and Tier | Python (not AI) scoring against criteria → clean Tier 1/2/3 output |
| 3 | Score Fit Fast | Read website/tech stack/hiring pages to reject bad-fit companies *before* spending on enrichment |
| 4 | Find Decision-Makers | Pulls contacts by title from data provider — 150+ contacts in 90 seconds |
| 5 | Enrich Contacts | Waterfall enrichment — cheapest provider first, cascades through 2–3 providers |
| 6 | Generate Copy | Reads email frameworks file, writes sequences, adjusts by industry/seniority/tier |
| 7 | Push Campaign | Creates campaign in sequencer via API, uploads leads, sets sequences, activates |
| 8 | Analyse and Improve | Pulls weekly analytics, identifies winners, updates email frameworks file automatically |

## GTM Tool Comparison: Claude Code vs Clay vs n8n vs Make vs Zapier

| Tool | Role | GTM sweet spot | Biggest weakness |
|------|------|----------------|-----------------|
| **Claude Code** ($20/mo) | "The Builder" | Writes/runs its own code; scores lists, calls any API, pushes to sequencers | Context resets between sessions; strategy still lives with you |
| **Clay** (~$167/mo) | "The Enricher" | Waterfall enrichment across 15+ providers; best email find rate | Credit costs spiral fast; not an automation engine, needs a trigger |
| **n8n** ($0) | "The Engine" | Open-source, full logic control, AI agent tools built in; website visitor → enrich → qualify → push to campaign, fully automated | Every API update = manual fix; managing 50+ client instances needs a dedicated person |
| **Make** ($9/mo) | "The Connector" | Visual builder, 1,000+ integrations; Webhook → Clay table → sequencer | Less flexible than n8n for complex logic; hits limits at very high data volumes |
| **Zapier** ($19.99/mo) | "The Glue" | 6,000+ integrations; every team member already knows it | Very expensive at scale; not built for complex GTM logic; outgrown quickly |

**How they work together:** Claude Code builds the logic → Clay enriches the data → n8n/Make/Zapier runs it 24/7.

## Clay vs Claude Code by GTM Stage

| Stage | Use | Mistake to avoid |
|-------|-----|-----------------|
| **Prospector** (testing messaging, need pipeline yesterday) | Clay | Ditching Clay to build custom Claude Code workflows before you know what messaging works |
| **Scaler** (repeatable playbook, growing team, need speed + control) | Clay as backbone + Claude Code for custom logic | Ditching Clay entirely because your GTM engineer says they can build it in Claude Code |
| **Operator** (dedicated engineering, millions in pipeline, stable processes) | Build custom, Clay optional | Still paying for tools when your team has capacity to own and maintain custom infrastructure |

## What NOT to Automate

| Automate | Keep Manual | Hybrid (AI drafts, human approves) |
|----------|-------------|-----------------------------------|
| Lead scraping and list building | Replying to warm prospects | ICP definition |
| Email enrichment and verification | Pricing and contract negotiation | Campaign copy |
| Pushing qualified leads to campaigns | Strategic account planning | Personalisation |
| Campaign performance reporting | Relationship building | Lead scoring (Claude runs logic, you set criteria) |
| CSV processing | First outreach to warm referrals | Call debrief |
| CRM updates after calls | Hiring and team decisions | Report interpretation |

## Cost Reality Check

| Workflow | Claude API | Third-party | Monthly at 4x/week |
|----------|-----------|------------|-------------------|
| Score 200 companies | ~$0.03 | None | ~$0.50 |
| Enrich 100 contacts (waterfall) | ~$0.05 | $5–15 | $20–60 |
| Generate 3-step sequences for 50 contacts | ~$0.08 | None | ~$1.30 |
| Personalise 100 icebreakers (Perplexity) | ~$0.40 | $5–10 | $20–40 |
| Full campaign build: source, score, enrich, copy, launch | ~$0.80 | $15–30 | $60–120 |
| Weekly campaign report | ~$0.10 | None | ~$1.60 |

**Total: $50–150/month. SDR equivalent: $4,000–7,000/month.**

## Key Limitations

- Runs per session, not continuously. For real-time monitoring, trigger via n8n, Zapier, or cron.
- No memory between sessions — CLAUDE.md and playbook files are your persistent memory.
- Multi-step pipelines break mid-way — add checkpoint saves every 50 leads.
- Rate limits at scale — add 1-second delays and process in chunks of 50 for 1,000+ lead runs.
- Context rot after ~2 hours. Use /clear at midpoint. Do hard thinking in the first half.

## Entities Mentioned

- [[Bill Stathopoulos]] — author
- [[SalesCaptain]] — the company
- [[Clay]] — enrichment layer
- [[Apollo]] — data provider for contacts
- [[Instantly]] — cold email sequencer
- [[HubSpot]] — CRM
- [[n8n]] — automation engine
- [[Trigify]] — signal platform
- [[Common Room]] — signal platform

## Concepts Touched

- [[ICP Avatar]] — the 3-level pain hierarchy framework
- [[GTM Engineering]] — this playbook operationalizes it for non-technical teams
- [[Hybrid AI Model]] — explicitly defined: what to automate, what to keep manual, what to do as hybrid
- [[Enrichment Waterfall]] — full 8-step pipeline includes it
- [[Schema-Governed LLM Behavior]] — CLAUDE.md is the GTM implementation of this concept

## See Also

- [[sources/salescaptain-linkedin-outbound-playbook]] — the companion LinkedIn-specific playbook
- [[ICP Avatar]] — the 3-level pain hierarchy, the most novel framework in this source
- [[GTM Engineering]] — the practice this playbook operationalizes
- [[Hybrid AI Model]] — the automation framework with explicit categories
- [[Bill Stathopoulos]] — author
