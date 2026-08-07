---
title: "Gemini"
type: entity
entity_kind: tool
tags: [tool, llm, google, multimodal]
created: 2026-07-28
updated: 2026-07-28
sources: [codyschneider-ad-library-gap-analysis]
---

# Gemini

*Google's multimodal LLM family; used here as an image/video describer rather than a text or code model.*

## Background

Google's LLM product line. This wiki has previously referenced Google AI products only as end-user video-generation tools ([[entities/veo3|Veo3]]); this is the first appearance of a Google LLM used for multimodal analysis/description within a GTM pipeline.

## Role in This Wiki

The description step in [[concepts/competitor-creative-gap-analysis|Cody Schneider's competitor creative gap analysis]]: after [[entities/apify|Apify]] scrapes competitor Facebook Ads Library creative, Gemini writes a description of each image/video focused specifically on angle, promise, and outcome — converting a pile of ad screenshots into a structured dataset Claude can then analyze for category-wide messaging gaps.

## Key Contributions / Actions

- Describes competitor ad creative (image and video) at the angle/promise/outcome level, per [[sources/codyschneider-ad-library-gap-analysis]].

## See Also

- [[concepts/competitor-creative-gap-analysis]] — the pipeline this tool's description step feeds
- [[entities/apify]] — upstream scraping step in the same pipeline
- [[entities/veo3]] — the wiki's other Google AI product, used for video generation rather than description
- [[sources/codyschneider-ad-library-gap-analysis]] — source
