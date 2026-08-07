---
title: "ClickHouse"
type: entity
entity_kind: tool
tags: [tool, data-warehouse, open-source, analytics, sql]
created: 2026-05-22
updated: 2026-05-22
sources: [codyschneider-marketing-agents-per-vertical]
---

# ClickHouse

An open-source columnar database designed for fast analytical queries. Used as the data warehouse in [[Cody Schneider]]'s recommended open-source marketing agent stack, paired with [[Airbyte]] for data ingestion.

## Role in This Wiki

The **storage and query layer** in the open-source GTM agent stack. Marketing agents write SQL against ClickHouse to retrieve the live business data they need to make channel decisions — ad performance, email metrics, revenue data, etc.

## Why Columnar

Columnar databases are optimized for analytical queries (aggregations, time-series, filtering across large datasets) rather than transactional workloads. This makes ClickHouse well-suited to the "agent writes SQL to analyze campaign performance" use case.

## Position in Stack

```
Airbyte (extract + load) → ClickHouse (store + query) → Agents (SQL → decisions)
```

## See Also

- [[Airbyte]] — the ingestion layer that feeds ClickHouse
- [[Data Warehouse for AI]] — the concept this implements
- [[sources/codyschneider-marketing-agents-per-vertical]] — primary source
- [[Graphed]] — Schneider's commercial alternative wrapping this infrastructure
