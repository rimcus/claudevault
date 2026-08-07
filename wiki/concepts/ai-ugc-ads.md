---
title: "AI UGC Ads"
type: concept
tags: [advertising, ugc, ai-video, facebook-ads, content-generation]
created: 2026-04-14
updated: 2026-07-28
sources: [codyschneider-ai-ugc-ads, codyschneider-fb-ads-ugc-playbook, codyschneider-transcript-personas, codyschneider-andromeda-b2b-facebook, codyschneider-ad-library-gap-analysis]
---

# AI UGC Ads

Video advertisements generated at scale using AI tools to mimic user-generated-content style — authentic-feeling, first-person, problem/solution format — without human creators. The pipeline combines pain point research, LLM scriptwriting, and AI video generation to produce 100+ ad variations per cycle.

## Overview

UGC-style ads (first person, casual, "I had this problem and found this solution") consistently outperform polished brand ads on social platforms. Traditionally they require recruiting, briefing, and paying human creators. AI UGC Ads replicate the format programmatically.

[[Cody Schneider]]'s pipeline uses Reddit as the pain point source (real customer language), Claude for scripts, and [[HeyGen]] for video generation — with [[Graphed]] tracking which ads drive actual Customer Lifetime Value.

## The Pipeline

```
Reddit (pain points) → [Exa AI scrape]
    → Claude (write scripts)
    → HeyGen API (generate video)
    → ffmpeg (remove silence)
    → json2video (add captions)
    → Facebook Ads (publish)
    → Graphed + PostHog + Stripe (measure CLV)
    → Remix winners
```

## Why Creative IS Targeting: The Andromeda Foundation

[[sources/codyschneider-andromeda-b2b-facebook]] (June 2026) provides the theoretical basis for the entire creative-volume approach. Meta's Andromeda algorithm update killed audience-first targeting. The algorithm now reads your creative and landing page, predicts who will convert from behavioral signals, and finds them — the marketer no longer specifies the audience. The creative specifies it implicitly.

**Implications for the UGC pipeline:**
- Each creative finds a different cohort of converters — one ad reaching one audience does not scale
- Creative packs (10+/week) are how you reach multiple buyer personas simultaneously
- This is why broad targeting ("target all of Facebook") works: Andromeda does the audience-finding
- Clean conversion events (signup + payment) are the signal that teaches the algorithm what "high intent" looks like

The moat moved from media-buying tricks to: **persona definitions + creative volume + data infrastructure.** All three are what the UGC pipeline produces.

## Why 100+ Variations Matters

Statistical significance on creative testing requires volume. At 5–10 ads, you're guessing at what works. At 100+, patterns emerge. The winning creative signals are real, not noise. Manual creative teams can't compete at this testing velocity.

## Key Optimization Metric: CLV, Not ROAS

Optimizing for Return on Ad Spend can surface ads that get cheap clicks but attract the wrong customers. Connecting ad data all the way through to Stripe revenue (via [[Graphed]]) surfaces ads that generate customers who *stay* and pay over time.

## PROTIP from Schneider

Build dedicated landing pages for winning ads. Message-to-page match (the ad's specific pain point is addressed on the landing page) dramatically improves conversion rates.

## Detailed Execution (June 2026 Update)

From [[sources/codyschneider-fb-ads-ugc-playbook]], the full tactical detail:

**Research (two sources, ranked):**
- **Best:** Sales call transcripts — mine 10, extract exact language, find 3–4 repeating motivations. Customer said it unprompted in a buying context. See [[sources/codyschneider-transcript-personas]].
- **Proxy when no transcripts:** Use Perplexity to search "pain points [x person] has for [y thing] that my [z product] solves reddit," then follow up for "exact quotes." Verbatim Reddit language is the next best thing.

**Persona → script mapping:** desire → hook, fear → body, belief → agreement before reframe. The demographic is the targeting layer, not the brief. See [[ICP Avatar]].

**Video tools:** [[HeyGen]] (original), plus now [[Seedance]] and [[Veo3]] (Google) as alternatives.

**Audience targeting:** Facebook Business Page Admins — high-signal B2B proxy for small business decision-makers.

**Campaign phasing:** Start with a **click campaign** (7 days, all creatives simultaneously). Promote winners to a **conversion campaign** with signup + payment events. This lets the algorithm find signal cheaply before committing spend to conversion optimization.

**Tracking stack:** Custom event → data layer → [[entities/google-tag-manager|Google Tag Manager]] → Facebook. Community warning: misfiring conversion events cause half of apparent "creative fatigue" — check the pixel before killing a winner.

## A Third Research Source: Competitor Creative (July 2026)

[[sources/codyschneider-ad-library-gap-analysis]] adds a research method that inverts the prior two (sales transcripts, Reddit pain points): instead of starting from the advertiser's own customer pain, it starts from what every competitor in the category is already claiming (via Facebook Ads Library, described by [[entities/gemini|Gemini]], gap-analyzed by Claude), and uses Reddit only afterward, to validate the ideated gap rather than to source it. See [[concepts/competitor-creative-gap-analysis]] for the full pipeline. It also documents a more autonomous closing loop than earlier UGC-ad sources: [[entities/graphed|Graphed]]'s MCP connected into Claude Code analyzes performance a day after launch, and Claude itself calls the Facebook Ads API to kill losers and reallocate budget to winners — then the whole loop is deployed to a server to run unattended.

## See Also

- [[sources/codyschneider-ai-ugc-ads]] — the original pipeline source (Exa + CLV measurement)
- [[sources/codyschneider-fb-ads-ugc-playbook]] — the execution detail (Perplexity research, targeting, click→conversion phasing, GTM tracking)
- [[sources/codyschneider-ad-library-gap-analysis]] — third research source (competitor creative) and a more autonomous optimization loop
- [[concepts/competitor-creative-gap-analysis]] — the sibling pipeline this section summarizes
- [[GTM Engineering]] — the practice context
- [[Growth Loop]] — the feedback cycle that improves the ads over time
- [[HeyGen]] — AI avatar video generation (original tool)
- [[Seedance]] — AI video generation alternative
- [[Veo3]] — Google's AI video generation model
- [[Graphed]] — the analytics layer
- [[Cody Schneider]] — defined this pipeline
