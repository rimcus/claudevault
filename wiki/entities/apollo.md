---
title: "Apollo"
type: entity
entity_kind: tool
tags: [tool, lead-enrichment, b2b, email, sales]
created: 2026-04-14
updated: 2026-04-14
sources: [codyschneider-gtm-agents]
---

# Apollo

A B2B sales intelligence and contact enrichment platform. Finds professional email addresses and company data given a name or LinkedIn profile. Used in [[Cody Schneider]]'s lead pipeline to enrich scraped LinkedIn engagers with emails.

## Pipeline Position

[[Apify]] (scrape) → **Apollo** (enrich + email) → [[entities/millionverifier|MillionVerifier]] (verify) → [[Instantly]] (send)

## See Also

- [[GTM Agents]] — the workflow context
- [[AI Marketing Stack]] — the broader stack
- [[Apify]] — feeds into Apollo
- [[entities/millionverifier|MillionVerifier]] — Apollo's output is verified here
