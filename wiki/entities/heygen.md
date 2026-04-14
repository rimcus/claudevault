---
title: "HeyGen"
type: entity
entity_kind: tool
tags: [tool, ai-video, ugc, content-generation]
created: 2026-04-14
updated: 2026-04-14
sources: [codyschneider-ai-ugc-ads]
---

# HeyGen

An AI video generation platform with an API. Used in [[Cody Schneider]]'s [[AI UGC Ads]] pipeline to convert Claude-written scripts into UGC-style videos at scale.

## Role in This Wiki

The video generation layer in the AI UGC ads pipeline. Takes a script (from Claude) and outputs a raw video, which is then post-processed by ffmpeg (silence removal) and json2video (captions) before publishing to Facebook Ads.

## Pipeline Position

Claude (script) → **HeyGen API** (generate video) → ffmpeg → json2video → Facebook Ads

## See Also

- [[AI UGC Ads]] — the workflow it powers
- [[GTM Engineering]] — the practice context
- [[Cody Schneider]] — uses it in his pipeline
