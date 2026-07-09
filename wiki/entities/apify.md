---
title: "Apify"
type: entity
entity_kind: tool
tags: [tool, web-scraping, lead-gen, automation, linkedin]
created: 2026-04-14
updated: 2026-07-09
sources: [codyschneider-gtm-agents, nickabraham-linkedin-inmail-pipeline]
---

# Apify

A web scraping and browser automation platform. Appears in two distinct pipeline roles: (1) scraping LinkedIn post engagers as a prospecting source, and (2) filtering LinkedIn contact lists for recent activity before InMail sends.

## Role in This Wiki

**Scraping layer** for LinkedIn post engager lists (Schneider GTM stack), and **activity filter** in Abraham's InMail pipeline — identifying contacts who posted or commented on LinkedIn in the last 30–60 days.

## Pipeline Positions

### GTM Agents (Schneider)

LinkedIn Post URL → **Apify** (scrape engagers) → [[Apollo]] (enrich + email) → [[Million Verifier]] (verify) → [[Instantly]] (send)

### LinkedIn InMail Pipeline (Abraham)

[[GetLeads]] (raw list) → [[NetNut]] (open-profile split) → **Apify** (active user filter: posted/commented in last 30–60 days) → AI agent (ICP fit) → sequencer

## Why Active User Filtering Matters

Active LinkedIn users (recent posts or comments) respond at significantly higher rates across all outbound channels — not just InMail. The Apify step is a behavioral signal filter: it applies a lightweight form of [[Signal Infrastructure]] to the send list before any message goes out.

## See Also

- [[sources/codyschneider-gtm-agents]] — original use case: scraping post engagers
- [[sources/nickabraham-linkedin-inmail-pipeline]] — second use case: active user filtering for InMail
- [[concepts/linkedin-inmail-pipeline|LinkedIn InMail Pipeline]] — the InMail system Apify filters within
- [[GTM Agents]] — the workflow where the original scraping role is used
- [[Apollo]] — next step in the Schneider engager pipeline
- [[entities/netnut|NetNut]] — upstream step in the Abraham InMail pipeline
