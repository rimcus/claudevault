---
title: "Maxime Champoux"
type: entity
entity_kind: person
tags: [well, qonto, ibanfirst, product-management, ai-coding, fintech]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# Maxime Champoux

*CEO/co-founder of [[entities/well|Well]]; 15 years in fintech — first employee at [[entities/ibanfirst|iBanFirst]] (built its first Core Banking system), then Head of Products at [[entities/qonto|Qonto]] for ~7 years, scaling its product org from 2 people to 150.*

## Background

Started as iBanFirst's first employee in a period before "startup" was a fashionable career path in France; built the company's first Core Banking system from scratch over 2.5 years, with no established playbook to reference. Specialized in payments APIs (pre-DSP2/open-banking) and, separately, shipped the first fully-online B2B account-opening flow at iBanFirst, including a compliance-timing "hack" (issuing the IBAN before full KYC/KYB completes, since the real risk is unauthorized payment, not merely holding an account number). Recruited into Qonto at ~50 employees specifically for this dual expertise — Qonto had inherited its onboarding flow from iBanFirst and needed both the onboarding know-how and Core Banking expertise to build its own in-house banking system, which he shipped in 6 months. Rose to Head of Products at Qonto, overseeing ~80% of the product surface directly or indirectly through his teams, before leaving in mid-2025 to found Well with co-founder Bastien Blanc (an ex-VP Engineering at a company heard as "Fintecture" in the transcript [low confidence on the exact name]).

## Role in This Wiki

The wiki's first practitioner voice on **AI-native engineering process** — distinct from both the cold-email/GTM-agent core and the general growth-marketing layer contributed by [[entities/luke-harries|Luke Harries]]. His account is unusual in including a specific, dated failure mode (a shipping-velocity plateau) and its fix (agent specialization by context window), rather than only success metrics.

## Key Contributions / Actions

- Built iBanFirst's first Core Banking system (2.5 years) and Qonto's replacement (6 months), crediting the acceleration to accumulated domain expertise, not a speed/quality trade-off.
- Scaled Qonto's product org from 2 to 150 people (~50 PMs at a ~1:8 PM-to-engineer ratio) during a period targeting velocity-as-competitive-moat.
- Founded Well: an AI agent platform building a unified "business context graph" for solopreneurs/SMBs.
- Took Well's 12-person team from ~7 to 100+ shipped features/month (Nov 2025–recording date) by moving the entire team onto direct AI-coding tools, then diagnosing and fixing a mid-transition quality plateau via named, specialized AI agents.

## Positions / Claims

| Claim | Source | Date |
|-------|--------|------|
| "Speed and quality are not a trade-off" | [[sources/maximechampoux-well-ai-native-engineering]] | 2026-07-22 (ingest date) |
| November 2025 (Opus 4.5) marked the shift from AI-augmented coding to "intent is what gets coded" | [[sources/maximechampoux-well-ai-native-engineering]] | 2026-07-22 |
| A feature can be "integrated" without being "assimilated" — the root cause of most AI-coding quality regressions his team saw | [[sources/maximechampoux-well-ai-native-engineering]] | 2026-07-22 |

## Relationships

- [[entities/well]] — CEO/co-founder
- [[entities/qonto]] — former Head of Products
- [[entities/ibanfirst]] — first employee, first Core Banking build
- [[entities/alex-olivet]] — podcast interviewer; first met ~8 years earlier at an early fintech
- [[concepts/agent-specialization-context-window]] — architect of this fix at Well
- [[concepts/toyota-production-system-for-software]] — carried this culture from Qonto into his own thinking

## See Also

- [[entities/well]] — the company he leads
- [[concepts/business-context-graph]] — Well's core product architecture
- [[concepts/roadmap-abstraction-shift]] — his own reworked product-management process
- [[sources/maximechampoux-well-ai-native-engineering]] — the primary source
