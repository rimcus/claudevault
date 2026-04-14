---
title: "Clay"
type: entity
entity_kind: tool
tags: [tool, gtm, enrichment, workflow, automation]
created: 2026-04-14
updated: 2026-04-14
sources: [alexvacca-gtm-engineering-hire, salescaptain-claude-code-gtm-playbook, salescaptain-linkedin-outbound-playbook]
---

# Clay

A data enrichment and workflow automation platform that is the central tool in the [[GTM Engineering]] stack. Allows building complex enrichment pipelines, enrichment waterfalls, and outbound workflows visually — without engineering tickets. Used by [[ColdIQ]] to run 80+ client campaigns from a single workspace.

## Role in This Wiki

The defining tool of the GTM engineer role. Vacca's hiring test: "Can they build a Clay workflow from scratch?" — this is the practical dividing line between a real GTM engineer and a retitled SDR. Cody Schneider uses a similar workflow-building approach with his Hermes Agent stack.

## Key Capabilities

- Build enrichment pipelines with multi-provider waterfalls
- Integrate with signal platforms (Common Room, Trigify, RB2B)
- Wire webhooks and route leads into sequences
- Stack firmographic, technographic, and intent data programmatically
- Run 80+ campaigns from a single workspace (ColdIQ's scale)

## The "Clay Test"

From [[Alex Vacca]]: the ability to build a Clay workflow from scratch is the practical hiring filter for GTM engineers. It requires understanding how enrichment outputs feed into sequencing — not just knowing Clay in isolation.

## Clay's Role in LinkedIn Workflows (SalesCaptain)

[[Bill Stathopoulos]] positions Clay as the orchestration hub in all 7 of [[SalesCaptain]]'s LinkedIn workflows. Every signal platform ([[Trigify]], [[Fibbler]], [[Teamfluence]], [[RB2B]]) routes detected signals into Clay for enrichment and qualification before any outreach is triggered.

## Clay vs. Claude Code (by GTM Stage)

From the SalesCaptain comparison:

| Stage | Recommendation |
|-------|---------------|
| Prospector (testing messaging) | Clay — fastest path to pipeline |
| Scaler (repeatable playbook) | Clay as backbone + Claude Code for custom logic |
| Operator (dedicated engineering) | Build custom; Clay optional |

**How they divide labor:** Claude Code builds the logic; Clay enriches the data; n8n/Make/Zapier runs it 24/7.

## Pricing Context

Clay costs ~$167/month. Biggest weakness: credit costs spiral fast at scale. It is an enrichment tool, not an automation engine — it needs a trigger (n8n, Make, Zapier) to run continuously.

## See Also

- [[GTM Engineering]] — the practice Clay enables
- [[Enrichment Waterfall]] — a core Clay pattern
- [[Signal Infrastructure]] — Clay is where signal data gets processed
- [[Alex Vacca]] / [[ColdIQ]] — most credible public user at scale
- [[Bill Stathopoulos]] / [[SalesCaptain]] — LinkedIn workflow implementation
- [[sources/salescaptain-claude-code-gtm-playbook]] — Clay vs. Claude Code comparison table
