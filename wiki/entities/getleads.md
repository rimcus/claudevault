---
title: "GetLeads"
type: entity
entity_kind: tool
tags: [tool, list-building, linkedin, outbound]
created: 2026-07-09
updated: 2026-07-09
sources: [nickabraham-linkedin-inmail-pipeline]
---

# GetLeads

A LinkedIn list-building tool. Used by [[Nick Abraham]] as Step 1 in the [[LinkedIn InMail Pipeline]] to pull the initial prospect list. For InMail campaigns, the only required output is the LinkedIn profile URL — no email or company data needed.

## Role in This Wiki

The list-pull layer of the InMail pipeline. Distinct from enrichment tools ([[NetNut]], [[Apify]], [[Apollo]]): GetLeads produces the raw URL list that subsequent steps qualify and filter.

## Pipeline Position

**GetLeads** (raw LinkedIn URL list) → [[NetNut]] (open-profile enrichment) → [[Apify]] (active user filter) → AI agent (ICP qualification) → sequencer

## See Also

- [[sources/nickabraham-linkedin-inmail-pipeline|Nick Abraham — LinkedIn InMail Pipeline]] — primary source
- [[concepts/linkedin-inmail-pipeline|LinkedIn InMail Pipeline]] — the full system this powers
- [[entities/netnut|NetNut]] — next step: open-profile enrichment
- [[entities/nick-abraham|Nick Abraham]] — the practitioner who documented this workflow
