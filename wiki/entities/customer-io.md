---
title: "Customer.io"
type: entity
entity_kind: tool
tags: [tool, email, esp, segmentation, lifecycle, saas]
created: 2026-04-14
updated: 2026-04-14
sources: [squeezeandscale-lemlist-email-nurturing]
---

# Customer.io

An email service platform (ESP) designed for product-triggered lifecycle messaging. Handles dynamic segmentation, behavioral flows, and high-volume sending. Central tool in [[Lemlist]]'s data-driven email nurturing stack.

## Role in This Wiki

The ESP layer in [[Behavioral Email Triggers]] systems. Receives behavioral data from a data warehouse (via webhook or sync), creates dynamic segments, and triggers email flows — without requiring engineering tickets for each new segment or flow.

## Key Capabilities

- Dynamic segments synchronized from an external data warehouse (e.g. BigQuery) — updated daily or in real time
- Webhook-based integration with orchestration tools (n8n)
- High volume handling — used at Lemlist's scale of 7M emails/year
- Variable injection — accepts custom fields (like the "LemCody" personalization variable) generated upstream

## When to Use

Nicolas (Lemlist) recommends Customer.io **at 1000+ users in database**. Below that threshold, simpler tools may be sufficient. The platform's strength is in managing complex, multi-flow behavioral systems at scale without becoming unmanageable.

## Position in Stack

```
BigQuery (behavior data) → Customer.io (segment + trigger) → webhook → n8n (enrich/personalize) → Customer.io (send with variable)
```

## See Also

- [[sources/squeezeandscale-lemlist-email-nurturing]] — primary source
- [[Lemlist]] — the company that built on top of it
- [[Behavioral Email Triggers]] — the system design Customer.io enables
- [[Data Warehouse for AI]] — the upstream data source that makes Customer.io segments behavioral rather than demographic
