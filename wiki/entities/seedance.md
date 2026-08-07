---
title: "Seedance"
type: entity
entity_kind: tool
tags: [tool, ai-video, ugc, ads]
created: 2026-06-16
updated: 2026-07-28
sources: [codyschneider-fb-ads-ugc-playbook, codyschneider-ad-library-gap-analysis]
---

# Seedance

An AI video generation tool. Listed alongside [[HeyGen]] and [[Veo3]] as an option for producing UGC-style ad videos from Claude-written scripts in [[Cody Schneider]]'s Facebook ads pipeline. Also used to generate video creative for [[concepts/competitor-creative-gap-analysis|competitor creative gap analysis]].

## Role in This Wiki

One of three AI video generation options in the [[AI UGC Ads]] pipeline. Takes a script as input and produces a video ad without human creators. In the competitor gap analysis pipeline, the input is a validated market gap rather than a Reddit-sourced script.

## Position in Stack

```
Reddit quotes → Claude (30-second UGC scripts) → Seedance (video) → Facebook Ads
```

```
Validated market gap → Seedance (video) → Facebook Ads (upload via API)
```

## See Also

- [[entities/heygen]] — alternative AI video generator; the original tool in the Schneider UGC pipeline
- [[entities/veo3]] — Google's AI video generator; the third option
- [[concepts/ai-ugc-ads]] — the concept this feeds into
- [[concepts/competitor-creative-gap-analysis]] — second use case: gap-fill creative generation
- [[sources/codyschneider-fb-ads-ugc-playbook]] — primary source
- [[sources/codyschneider-ad-library-gap-analysis]] — second source
