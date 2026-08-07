---
title: "Exa AI"
type: entity
entity_kind: tool
tags: [tool, search-api, scraping, ai-agents]
created: 2026-07-28
updated: 2026-07-28
sources: [codyschneider-twitter-outreach-pipeline, codyschneider-ai-ugc-ads, codyschneider-ad-library-gap-analysis]
---

# Exa AI

*AI-native search/scraping API used across multiple Schneider GTM pipelines as the retrieval step for Twitter profiles and Reddit content.*

## Background

A search API built for LLM-agent use rather than human browsing — returns structured, retrievable results an agent can act on directly. Appears in this wiki only through [[entities/cody-schneider|Cody Schneider]]'s pipelines; no independent source on Exa AI itself has been ingested.

## Role in This Wiki

A recurring retrieval-layer tool across three separate Schneider pipelines, each time doing a different job:
- **Twitter Outreach Pipeline** ([[sources/codyschneider-twitter-outreach-pipeline]]): finds a Twitter engager's LinkedIn profile, the step that turns an anonymous post-engager into an addressable lead.
- **AI UGC Ads** ([[sources/codyschneider-ai-ugc-ads]]): scrapes Reddit for pain-point language used as ad-script source material.
- **Competitor Creative Gap Analysis** ([[sources/codyschneider-ad-library-gap-analysis]]): scrapes Reddit to validate whether an LLM-ideated market gap corresponds to a real, expressed pain point.

Despite this recurrence, this is the first source dense enough in Exa-specific detail to warrant a dedicated entity page — prior mentions were single-line pipeline steps.

## Key Contributions / Actions

- Twitter engager → LinkedIn profile lookup, in the earliest Schneider pipeline in this wiki.
- Reddit scraping for pain-point research, in the AI UGC Ads pipeline.
- Reddit scraping for gap validation, in the competitor creative gap analysis pipeline.

## See Also

- [[concepts/ai-ugc-ads]] — pipeline using Exa AI for pain-point research
- [[concepts/competitor-creative-gap-analysis]] — pipeline using Exa AI for gap validation
- [[sources/codyschneider-twitter-outreach-pipeline]] — original use case
- [[entities/cody-schneider]] — uses Exa AI across all three pipelines
