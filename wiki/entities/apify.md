---
title: "Apify"
type: entity
entity_kind: tool
tags: [tool, web-scraping, lead-gen, automation]
created: 2026-04-14
updated: 2026-04-14
sources: [codyschneider-gtm-agents]
---

# Apify

A web scraping and browser automation platform. Used in [[Cody Schneider]]'s [[GTM Agents]] stack to scrape LinkedIn post engagers as the first step in the lead generation pipeline.

## Role in This Wiki

The scraping layer of the LinkedIn lead pipeline: given a post URL, Apify extracts everyone who engaged with it as a prospecting list.

## Pipeline Position

LinkedIn Post URL → **Apify** (scrape engagers) → [[Apollo]] (enrich + email) → [[Million Verifier]] (verify) → [[Instantly]] (send)

## See Also

- [[GTM Agents]] — the workflow it powers
- [[AI Marketing Stack]] — the broader stack
- [[Apollo]] — next step in the lead pipeline
