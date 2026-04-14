---
title: "Trigify"
type: entity
entity_kind: tool
tags: [tool, signals, linkedin, gtm, intent]
created: 2026-04-14
updated: 2026-04-14
sources: [salescaptain-linkedin-outbound-playbook, alexvacca-gtm-engineering-hire]
---

# Trigify

A LinkedIn signal platform that detects and routes engagement events in real time — specifically post engagers, profile interactions, and keyword activity. The primary signal source in [[SalesCaptain]]'s content harvesting and keyword engager workflows.

## Role in This Wiki

Trigify is the LinkedIn-specific signal layer in [[Signal Infrastructure]]. Where [[Common Room]] and [[RB2B]] capture broader intent signals, Trigify specializes in LinkedIn behavioral data: who engaged with which content, who posted about specific problems, who is showing interest in your ICP topics.

## Key Use Cases (from SalesCaptain's 7 Workflows)

| Workflow | What Trigify captures |
|----------|----------------------|
| LinkedIn Harvesting (Workflow 02) | Prospect engages with your content 3+ times |
| Keyword Engagers (Workflow 04) | Someone posts or comments about problems you solve |

## Position in Stack

```
Trigify (detect engagement) → Clay (enrich, qualify) → HeyReach/Lemlist (send)
```

## See Also

- [[sources/salescaptain-linkedin-outbound-playbook]] — 7 workflows
- [[sources/alexvacca-gtm-engineering-hire]] — also mentions Trigify as a signal platform
- [[Signal Infrastructure]] — the concept this tool implements
- [[Clay]] — downstream enrichment layer
- [[RB2B]] — complementary signal tool (website visitors)
- [[Common Room]] — complementary signal tool (broader intent)
