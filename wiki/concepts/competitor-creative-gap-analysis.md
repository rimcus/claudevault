---
title: "Competitor Creative Gap Analysis"
type: concept
tags: [facebook-ads, competitive-intelligence, gap-analysis, ai-agents, gtm-engineering]
created: 2026-07-28
updated: 2026-07-28
sources: [codyschneider-ad-library-gap-analysis]
---

# Competitor Creative Gap Analysis

*Scrape every competitor's ad creative in a category, have an LLM describe what each ad is actually claiming, find the angle nobody is using, validate it against real complaints, then build and run ads directly in that gap — closed autonomously by a performance-analysis agent that kills losers and scales winners.*

## Overview

[[entities/cody-schneider|Cody Schneider]]'s method inverts the usual order of operations for ad creative research. His earlier [[concepts/ai-ugc-ads|AI UGC Ads]] pipeline starts from the advertiser's own customer pain (Reddit posts, sales-call transcripts) and writes creative from that. This method starts from the *competitive field* — what every other player in the category is already saying — and looks for the claim nobody has made yet. Reddit is still used, but demoted to a validation step at the end of the ideation phase rather than the primary research source.

The mechanism that makes this tractable at scale is using an LLM as a structured describer of unstructured ad creative: instead of a human manually reviewing dozens of competitor ads, [[entities/gemini|Gemini]] converts each image/video into a consistent description schema (angle, promise, outcome), which turns a pile of screenshots into a queryable dataset Claude can pattern-match across for gaps.

This shares its raw data source (Facebook Ads Library) with the wiki's existing [[concepts/ad-library-market-validation]] concept, but the two use it for opposite purposes: that concept asks "is anyone already making money in this space" to decide *whether to build a product*; this concept asks "what is everyone in this space already saying" to decide *what to say that they aren't*, for a product that already exists.

## Key Properties / Characteristics

- Research order is inverted relative to prior Schneider ad pipelines: competitor claims first, customer-pain validation second (vs. Reddit/transcripts first in [[concepts/ai-ugc-ads]]).
- Uses an LLM as a structured annotator of visual/video creative (angle, promise, outcome) rather than as a copywriter — the generation step comes later.
- Gap validation is a distinct step from gap ideation — Claude proposes gaps, Exa AI/Reddit confirms they correspond to real expressed pain before any creative is built.
- The full loop — scrape, describe, find gap, validate, generate, launch, analyze, reallocate budget — is designed to run once manually, then be deployed to a server to repeat autonomously.

## How It Works

1. Scrape every competitor's Facebook Ads Library creative via the [[entities/apify|Apify]] API.
2. [[entities/gemini|Gemini]] writes a description of each image/video, focused specifically on angle, promise, and outcome.
3. The resulting set of descriptions is a map of how the category talks about itself.
4. Claude analyzes the map to identify gaps — angles or promises the category isn't using.
5. Validate each ideated gap by scraping Reddit via [[entities/exa-ai|Exa AI]] for evidence the gap reflects a real, expressed pain point.
6. Generate ad creative built around the validated gap using [[entities/nano-banana|Nano Banana]] (images) and [[entities/seedance|Seedance]] (video).
7. Upload the ads to Facebook directly via API key.
8. One day later: connect [[entities/graphed|Graphed]]'s MCP into Claude Code to analyze what's working.
9. Claude calls the Facebook Ads API to turn off losing creative and move winners into their own ad sets with dedicated budget.
10. Once proven, deploy the whole loop to a server so it runs and re-optimizes on its own.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/codyschneider-ad-library-gap-analysis]] | The described pipeline is Schneider's current ("today") GTM engineering method | low (no metrics, results, or timeframe given anywhere in the post — the only source of the wiki's Schneider corpus with zero supporting numbers) |

## Contradictions & Open Questions

- No result numbers of any kind (spend, CTR, CPM, CAC, revenue) — every other Schneider source in this wiki anchors at least one claim with a metric; this one doesn't, which weakens confidence relative to his other posts.
- "Have Claude analyze where the gaps are" is asserted as a capability without detail on the analysis method (embedding clustering? prompted pattern-matching over the whole description set? single-pass reasoning?) — the mechanism is a black box.
- No mention of how many competitors/ads constitute a sufficient map before gap-finding is reliable, or how often the competitor map itself needs refreshing as competitors launch new creative.
- The autonomous deploy-to-a-server step raises the same open question already logged against [[concepts/gtm-agents]]: no source yet (including this one) addresses what happens when the agent's gap ideation or budget-reallocation decisions are wrong, or how a human would catch it.

## See Also

- [[sources/codyschneider-ad-library-gap-analysis]] — primary source
- [[concepts/ai-ugc-ads]] — sibling pipeline; same output (Facebook UGC-style ads) via the opposite research order (customer-pain-first vs. competitor-claims-first)
- [[concepts/ad-library-market-validation]] — same raw data source (Facebook Ads Library), used for product-idea validation rather than creative gap-finding
- [[concepts/gtm-agents]] — the broader autonomous-agent thesis; this pipeline's "deploy to a server" closing step is a direct instance
- [[entities/apify]], [[entities/gemini]], [[entities/exa-ai]], [[entities/nano-banana]], [[entities/seedance]], [[entities/graphed]] — the tool chain
