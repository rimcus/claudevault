---
title: "Data Warehouse for AI"
type: concept
tags: [data, infrastructure, ai-agents, gtm, decision-making]
created: 2026-04-14
updated: 2026-04-14
sources: [codyschneider-gtm-agents, squeezeandscale-lemlist-email-nurturing, codyschneider-marketing-agents-per-vertical]
---

# Data Warehouse for AI

The practice of centralizing all business data (conversion events, campaign performance, user behavior, revenue) into a queryable warehouse so that AI agents can access it as context for decisions. The key architectural insight from [[Cody Schneider]]'s [[GTM Agents]] framework: **agents without data context are guessing; agents with a warehouse are optimizing.**

## Overview

Most AI agent demos operate on isolated inputs — "here's a URL, summarize it." Real business agents need cross-domain context: to optimize Google Ads, the agent needs to know which keywords are converting to paid users, not just which keywords have high clicks. That data lives in the warehouse.

The warehouse is the bridge between scattered business data and agent intelligence. It is the shared memory layer for the entire [[AI Marketing Stack]].

## What Goes In

- Conversion events (signups, trials, payments) from product analytics ([[PostHog]])
- Ad campaign performance (spend, clicks, conversions)
- Email campaign metrics (open rates, activation by sequence)
- SEO performance (rankings, traffic, revenue attribution)
- CRM data ([[HubSpot]] contacts, deal stages)

## What Agents Get Out

- "Which landing pages drove the most paid conversions last 30 days?" → informs which pages to build more of
- "Which ad creative has the best cost-per-activation?" → informs what to promote vs. kill
- "Which email sequence step has the highest drop-off?" → informs nurture optimization
- "Which blog posts drove signups?" → informs future content topics

## Key Properties

- **Single source of truth** for all agents — prevents conflicting decisions
- **Open-source options** make this accessible without enterprise tooling
- **Queryable by LLM** — agents can write SQL or use structured APIs to retrieve context

## Real-World Implementation (Lemlist)

[[Lemlist]]'s email marketing stack provides a concrete implementation: **BigQuery** (or "Wind Data Warehouse") nourished directly by product events. The data team creates pre-processed tables (user email + behavior metrics) for the marketing team to use without writing raw queries. These tables feed [[Customer.io]] with daily syncs, powering dynamic behavioral segments.

This confirms the warehouse as a **product-adjacent infrastructure layer** — it's not just for outbound GTM, but for the entire SaaS lifecycle (activation, retention, expansion, advocacy).

## The Open-Source Stack (Now Named)

Schneider's May 2026 post names the specific open-source stack he recommends:

**[[Airbyte]] + [[ClickHouse]]**

- **Airbyte** — open-source data pipeline; extracts from all business data sources and loads into the warehouse
- **ClickHouse** — open-source columnar database; fast for analytical SQL queries

This resolves the wiki's standing open question about which open-source warehouse Schneider uses.

**Setup caveat (from community):** Getting clean, reliable live business data piped correctly is a **2–3 week setup minimum** for most companies — even with Airbyte + ClickHouse. The tooling is accessible; the data hygiene and integration work is not trivial.

**Implementation spectrum:**
- Open-source: Airbyte + ClickHouse (self-managed)
- Cloud/managed: BigQuery (Lemlist's choice)
- Commercial: [[Graphed]] (Schneider's own product; wraps this infrastructure with a managed service)

## Open Questions

- How does the warehouse stay in sync in real time vs. batch? Lemlist does daily batch syncs into Customer.io — real-time not required for lifecycle email. For ad optimization, faster sync may matter more.

## The SMB-Scale Variant (Well)

[[sources/maximechampoux-well-ai-native-engineering]] applies this same "centralize scattered data so agents have real context" thesis to a segment this concept's other sources don't address: solopreneurs and small businesses who will never build (or afford) an Airbyte + ClickHouse warehouse or hire a data team. [[entities/well|Well]]'s [[concepts/business-context-graph]] is the SMB-scale equivalent — a unified data model built via an MCP-first, demand-driven connector waterfall rather than a formal ETL pipeline, aimed at giving AI agents (invoice retrieval, financial forecasting) the same kind of cross-domain context this concept describes at company scale.

## See Also

- [[AI Marketing Stack]] — the broader infrastructure context
- [[GTM Agents]] — the agents that query this warehouse
- [[Behavioral Email Triggers]] — the lifecycle email system the warehouse enables internally
- [[Airbyte]] — the open-source ingestion layer
- [[ClickHouse]] — the open-source warehouse layer
- [[Cody Schneider]] — identified this as the critical enabling layer for outbound GTM agents
- [[Lemlist]] — real-world implementation: BigQuery → Customer.io → behavioral flows
- [[concepts/business-context-graph]] — the SMB-scale variant of this same thesis
- [[sources/codyschneider-gtm-agents]] — Schneider's original GTM agents framework
- [[sources/codyschneider-marketing-agents-per-vertical]] — names Airbyte + ClickHouse
- [[sources/squeezeandscale-lemlist-email-nurturing]] — Lemlist's concrete BigQuery implementation
- [[sources/maximechampoux-well-ai-native-engineering]] — the SMB-scale variant
