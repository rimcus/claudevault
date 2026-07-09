---
title: "NetNut"
type: entity
entity_kind: tool
tags: [tool, enrichment, linkedin, inmail, outbound]
created: 2026-07-09
updated: 2026-07-09
sources: [nickabraham-linkedin-inmail-pipeline]
---

# NetNut

A LinkedIn enrichment API that flags whether a profile has Open Profile enabled. The critical gate in the [[LinkedIn InMail Pipeline]]: it determines who can receive a free InMail and who would cost a paid credit.

## Role in This Wiki

The segmentation layer of the InMail pipeline. Without this step, non-open profiles enter the sequencer and silently burn paid InMail credits — the failure mode that triggers LinkedIn's credit freeze and halts all sending.

## Key Behavior

- Returns open-profile status per LinkedIn URL
- Output splits the list into two buckets: open (free to message) and non-open (paid credit required)
- Status is not permanent: a profile flagged as open today may flip to closed before send time; sequencers must recheck at send

## Pipeline Position

[[GetLeads]] (raw list) → **NetNut** (open-profile enrichment + split) → [[Apify]] (active user filter) → AI agent → sequencer

## See Also

- [[sources/nickabraham-linkedin-inmail-pipeline|Nick Abraham — LinkedIn InMail Pipeline]] — primary source
- [[concepts/linkedin-inmail-pipeline|LinkedIn InMail Pipeline]] — the full system this enables
- [[entities/getleads|GetLeads]] — upstream: raw list pull
- [[entities/apify|Apify]] — downstream: active user filter
- [[entities/nick-abraham|Nick Abraham]] — the practitioner who documented this use
