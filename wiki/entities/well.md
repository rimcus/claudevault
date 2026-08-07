---
title: "Well"
type: entity
entity_kind: organization
tags: [ai-agents, smb, accounting, business-context-graph, mcp]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# Well

*AI agent platform building a unified "business context graph" for solopreneurs and small businesses; co-founded by [[entities/maxime-champoux|Maxime Champoux]] and Bastien Blanc. Company name appears once in the source transcript as "Weal" — likely a transcription artifact [low confidence on exact spelling].*

## Background

Founded by Champoux after leaving [[entities/qonto|Qonto]], carrying over his stated mission there: reduce administrative burden for entrepreneurs so they have more time for the actual business. Started narrower — agents that auto-retrieve missing invoices via email, WhatsApp, and browser automation for monthly bookkeeping close — then generalized into a full unified data model spanning bank transactions, suppliers, customers, accounting, and subscriptions once the team realized the invoice-retrieval agents needed that broader context to work reliably. Co-founder Bastien Blanc is described as the former VP Engineering at a company heard as "Fintecture" in the transcript [low confidence].

## Role in This Wiki

The wiki's first case study in **AI-native engineering process** at the company-building level: a small (12-person) team's month-by-month velocity transformation (7 → 100+ shipped features/month), including the specific quality plateau it hit and the fix. Also the source of the wiki's first "business context graph" concept — a data-centralization thesis parallel to [[concepts/data-warehouse-for-ai]] but aimed at a segment that can't afford a real data warehouse.

## Key Contributions / Actions

- Runs [[concepts/business-context-graph]]: unified SMB data model built via an MCP-first, demand-driven connector waterfall (existing MCP → generate from API docs → browser-extension fallback).
- Runs [[concepts/ai-native-engineering-team]]: 100% of the team (including designers and the CEO) codes directly via Claude Code, under bounded permissions and full-team buy-in.
- Runs [[concepts/agent-specialization-context-window]]: 8 named, stable, domain-specialized coding agents plus an orchestrator, the fix for a shipping-velocity plateau at 40–50 features/month.
- Exposes its own MCP connectors directly inside Claude, letting a user connect to their unified business context through a single Well MCP channel with persistent auth.
- Platform is free to use until September (year unspecified, presumably 2026, per the recording).

## Positions / Claims

| Claim | Source | Date |
|-------|--------|------|
| Went from 7 to 100+ shipped features/month between November 2025 and the recording date, with the same 12-person team | [[sources/maximechampoux-well-ai-native-engineering]] | 2026-07-22 (ingest date) |
| Connectors are built demand-driven per customer signal, not pre-built speculatively for every SaaS tool | [[sources/maximechampoux-well-ai-native-engineering]] | 2026-07-22 |

## Relationships

- [[entities/maxime-champoux]] — CEO/co-founder
- [[entities/qonto]] — Champoux's prior employer; source of much of Well's engineering culture
- [[concepts/business-context-graph]] — core product architecture
- [[concepts/agent-specialization-context-window]] — internal engineering practice

## See Also

- [[entities/maxime-champoux]] — CEO/co-founder
- [[concepts/business-context-graph]] — the product
- [[concepts/ai-native-engineering-team]] — the engineering culture
- [[sources/maximechampoux-well-ai-native-engineering]] — the primary source
