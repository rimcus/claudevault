---
title: "ICP Avatar"
type: concept
tags: [gtm, icp, copy, outbound, targeting, saas]
created: 2026-04-14
updated: 2026-04-14
sources: [salescaptain-claude-code-gtm-playbook]
---

# ICP Avatar

A framework for defining an ideal customer profile that goes beyond company-type descriptions to identify *why someone buys today*. Developed by [[Bill Stathopoulos]] / [[SalesCaptain]]. The core insight: most ICPs are useless because they describe a company without naming the buying trigger.

## The Problem With Standard ICPs

Standard ICPs ("Series B SaaS companies with 50–200 employees in fintech") describe *who could buy* but not *when they buy* or *what makes them buy right now*. This produces generic outreach that reaches the right companies at the wrong moment with the wrong message.

## The 3-Level Pain Hierarchy

Every ICP Avatar is built around three nested pain levels:

| Level | What it is | Example (sales ops tool) |
|-------|-----------|--------------------------|
| **Surface pain** | Symptom they describe when asked "what's the problem?" | "Our reporting takes too long" |
| **Operational pain** | Downstream business cost of the surface pain | "We're making quota decisions on stale data" |
| **Identity-level pain** | What this says about them as a professional — the real buy trigger | "I look incompetent in front of the board every quarter" |

The identity-level pain is where deals actually close. Surface pain gets you noticed. Operational pain gets you in a meeting. Identity-level pain triggers urgency.

## The Quote Rule

**Every phrase must come from an exact customer quote.** "They struggle with follow-up" is analysis. "Our follow-up is a mess" is a quote. The distinction matters because customers respond to their own language — paraphrased analysis sounds like marketing copy.

**Sources for quotes:**
- Call transcripts
- Deal notes
- G2 / Capterra reviews
- Lost deal notes
- Onboarding calls

## How Claude Code Uses the ICP Avatar

In [[SalesCaptain]]'s implementation, the ICP Avatar is stored as a playbook file. Claude Code reads it when generating copy, scoring leads, or routing sequences — ensuring every output is grounded in real buyer language rather than generic benefit statements.

## Relation to Hybrid AI Model

The ICP Avatar is one of [[Stathopoulos]]'s explicit "keep human" items: ICP definition belongs in the hybrid column (AI drafts, human approves) — not the automate column. The human judgment about which quotes are representative is load-bearing.

## See Also

- [[sources/salescaptain-claude-code-gtm-playbook]] — primary source
- [[Bill Stathopoulos]] — originator
- [[Hybrid AI Model]] — ICP definition is the "hybrid" category (AI drafts, human approves)
- [[Cold Email Personalization Problem]] — ICP Avatar is the upstream fix for generic AI copy
- [[Schema-Governed LLM Behavior]] — the ICP Avatar is stored as a playbook Claude reads at runtime
