---
title: "Airbyte"
type: entity
entity_kind: tool
tags: [tool, data-pipeline, open-source, data-warehouse]
created: 2026-05-22
updated: 2026-05-22
sources: [codyschneider-marketing-agents-per-vertical]
---

# Airbyte

An open-source data pipeline tool that extracts data from multiple sources and loads it into a central data warehouse. Used alongside [[ClickHouse]] as the recommended open-source stack for [[Cody Schneider]]'s marketing agent data warehouse.

## Role in This Wiki

The **extraction and loading layer** in the Airbyte + ClickHouse stack. Airbyte pulls live business data (CRM, ad platforms, email, product analytics) into ClickHouse so that marketing agents can query it via SQL.

## Position in Stack

```
Business data sources (CRM, ads, email, product) → Airbyte (extract + load) → ClickHouse (warehouse) → Agents (SQL queries)
```

## See Also

- [[ClickHouse]] — the warehouse Airbyte loads data into
- [[Data Warehouse for AI]] — the concept this implements
- [[sources/codyschneider-marketing-agents-per-vertical]] — primary source
- [[Graphed]] — Schneider's commercial alternative to this open-source stack
