---
title: "Business Context Graph"
type: concept
tags: [data-model, smb, mcp, ai-agents, accounting, unified-data]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# Business Context Graph

*A unified data model spanning bank transactions, suppliers, customers, contacts, accounting, and subscriptions — an ERP-equivalent layer for businesses too small to ever buy a real ERP or build a data warehouse.*

## Overview

The core product architecture of [[entities/maxime-champoux|Maxime Champoux]]'s startup [[entities/well|Well]]. The product started narrower — browser/email/WhatsApp agents that automatically retrieve missing invoices, cutting a monthly bookkeeping close from 2–5 hours to about 2 minutes — but building that surfaced a harder dependency: the agents needed *context* (which invoices are actually missing) that only exists if you already have the bank transaction feed, existing invoice history, and a transaction-categorization layer. Pulling that thread led to generalizing the whole thing into a unified data model, explicitly modeled on how Attio built a single unified data model for the CRM category (not a wiki entity page), but applied beyond CRM to the entrepreneur's entire operating context.

This is the wiki's second documented instance of "centralize scattered business data so agents have real context" (the first being [[concepts/data-warehouse-for-ai]] from the cold-email/GTM side of the wiki) — but aimed at a segment (solopreneurs, small businesses) that structurally cannot afford the first instance's solution (a company-scale data warehouse, 2–3 week setup minimum per that concept's existing evidence).

## Key Properties / Characteristics

- Single unified data model across: bank transactions, suppliers, customers, contact points, accounting, subscriptions/billing.
- Explicitly targets a segment (SMB/solopreneur) that has no data warehouse and no centralized data by default — data is scattered across whatever tools the entrepreneur happens to use.
- Connector acquisition is MCP-first and demand-driven (see below), not pre-built speculatively for every possible SaaS tool.
- Categorization layer filters signal from noise — most bank transactions need a supporting invoice/receipt; small or internal transfers typically don't.

## How It Works

**The connector waterfall.** In priority order: (1) use an existing MCP connector, pulled automatically from public MCP directories, if one already exists for the tool; (2) if none exists, generate a connector from the tool's own API documentation; (3) if there's no API documentation either, fall back to a Chrome browser extension that performs the needed actions via vision models or scripts.

**Demand-driven, not speculative.** Well does not attempt to pre-integrate with the entire SaaS universe up front. New connectors get built reactively, triggered by real customer signal — a bank transaction pattern, or an email referencing a tool the customer clearly uses that Well doesn't support yet — which then runs through the same three-step waterfall to close the specific gap.

**What the graph unlocks once populated:** automated invoice-matching/monthly close; agentic actions layered on top (e.g., CRM-style automations, financial-report generation); natural-language financial forecasting ("what's my cash burn, what happens to my runway if I hire a brand designer") without the entrepreneur manually maintaining a spreadsheet, pulling every data source by hand, consolidating, and building scenario assumptions — work Champoux says otherwise takes hours per iteration.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/maximechampoux-well-ai-native-engineering]] | The original invoice-retrieval agent cut monthly close from 2–5 hours to ~2 minutes | medium (practitioner claim, ElevenLabs-source-style specificity but no independent verification) |
| [[sources/maximechampoux-well-ai-native-engineering]] | Connectors are built demand-driven per customer signal rather than pre-built for the full SaaS universe | high (explicit, direct architectural claim from the founder) |

## Contradictions & Open Questions

- No detail on how Well handles conflicting or duplicate entities across sources (e.g., the same supplier appearing under slightly different names in the bank feed vs. an invoice PDF vs. a CRM) — a common hard problem for any unified-data-model approach.
- Open question: what's the actual reliability/error rate of the browser-extension fallback (vision/scripts) tier of the connector waterfall, versus the MCP and API-doc tiers? The source doesn't distinguish confidence levels across the three tiers.

## See Also

- [[concepts/data-warehouse-for-ai]] — the wiki's existing "centralize business data for agent context" concept, built for company-scale GTM use rather than SMB back-office use
- [[concepts/ai-native-engineering-team]] — how Well's own engineering team is built to ship this product at high velocity
- [[entities/well]] — the product this concept describes
- [[sources/maximechampoux-well-ai-native-engineering]] — primary source
