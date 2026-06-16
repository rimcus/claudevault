---
title: "AI UGC Ads"
type: concept
tags: [advertising, ugc, ai-video, facebook-ads, content-generation]
created: 2026-04-14
updated: 2026-04-14
sources: [codyschneider-ai-ugc-ads, codyschneider-fb-ads-ugc-playbook]
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

## Why 100+ Variations Matters

Statistical significance on creative testing requires volume. At 5–10 ads, you're guessing at what works. At 100+, patterns emerge. The winning creative signals are real, not noise. Manual creative teams can't compete at this testing velocity.

## Key Optimization Metric: CLV, Not ROAS

Optimizing for Return on Ad Spend can surface ads that get cheap clicks but attract the wrong customers. Connecting ad data all the way through to Stripe revenue (via [[Graphed]]) surfaces ads that generate customers who *stay* and pay over time.

## PROTIP from Schneider

Build dedicated landing pages for winning ads. Message-to-page match (the ad's specific pain point is addressed on the landing page) dramatically improves conversion rates.

## Detailed Execution (June 2026 Update)

From [[sources/codyschneider-fb-ads-ugc-playbook]], the full tactical detail:

**Research:** Use Perplexity to search "pain points [x person] has for [y thing] that my [z product] solves reddit," then follow up for "exact quotes." This surfaces verbatim Reddit language — the raw input for scripts that sound like real customers.

**Video tools:** [[HeyGen]] (original), plus now [[Seedance]] and [[Veo3]] (Google) as alternatives.

**Audience targeting:** Facebook Business Page Admins — high-signal B2B proxy for small business decision-makers.

**Campaign phasing:** Start with a **click campaign** (7 days, all creatives simultaneously). Promote winners to a **conversion campaign** with signup + payment events. This lets the algorithm find signal cheaply before committing spend to conversion optimization.

**Tracking stack:** Custom event → data layer → Google Tag Manager → Facebook. Community warning: misfiring conversion events cause half of apparent "creative fatigue" — check the pixel before killing a winner.

## See Also

- [[sources/codyschneider-ai-ugc-ads]] — the original pipeline source (Exa + CLV measurement)
- [[sources/codyschneider-fb-ads-ugc-playbook]] — the execution detail (Perplexity research, targeting, click→conversion phasing, GTM tracking)
- [[GTM Engineering]] — the practice context
- [[Growth Loop]] — the feedback cycle that improves the ads over time
- [[HeyGen]] — AI avatar video generation (original tool)
- [[Seedance]] — AI video generation alternative
- [[Veo3]] — Google's AI video generation model
- [[Graphed]] — the analytics layer
- [[Cody Schneider]] — defined this pipeline
