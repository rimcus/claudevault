---
title: "GTM Engineering Today: Competitor Ad Library → Gap Analysis → Autonomous Ads"
type: source
tags: [gtm-engineering, facebook-ads, competitive-intelligence, ai-agents, cody-schneider]
created: 2026-07-28
updated: 2026-07-28
sources: [codyschneider-ad-library-gap-analysis]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2081877301894025717"
source_type: other
---

# GTM Engineering Today: Competitor Ad Library → Gap Analysis → Autonomous Ads

**Author:** [[entities/cody-schneider|Cody Schneider]]
**Date:** 2026-07-28
**Source:** [x.com/codyschneider/status/2081877301894025717](https://x.com/codyschneider/status/2081877301894025717)

## Core Thesis

Positioning gaps in a competitive category can be found mechanically — scrape every competitor's Facebook Ads Library creative, have an LLM describe what each ad is actually claiming (angle, promise, outcome), and hand that map to Claude to find what nobody in the category is saying. Validate the gap against real complaints on Reddit, then generate and run ads directly in that gap. Once the loop is proven manually, deploy it to a server so it re-runs and self-optimizes without a human in it.

## Key Points

- **Map the category's claims:** Pull every competitor's Facebook Ads Library creative via the [[entities/apify|Apify]] API, then have [[entities/gemini|Gemini]] write descriptions of each image/video — specifically the angle, the promise, and the outcome each ad is selling. The output is a map of how the whole category talks about itself.
- **Find the gap:** Feed that map to Claude and have it identify where the market's messaging has gaps — angles or promises nobody in the category is using.
- **Validate the gap:** Before building creative around an ideated gap, scrape Reddit via [[entities/exa-ai|Exa AI]] to check whether the gap corresponds to a real, expressed pain point rather than a theoretical one.
- **Generate and launch:** Use [[entities/nano-banana|Nano Banana]] and [[entities/seedance|Seedance]] to produce ads built around the validated gap, then upload them to Facebook directly via API key — no manual ad-manager work.
- **Close the loop autonomously:** One day later, connect [[entities/graphed|Graphed]]'s MCP into Claude Code to analyze performance. Claude then calls the Facebook Ads API directly to turn off losing creative and move winners into their own ad sets with dedicated budget.
- **Deploy:** once the system is proven working end to end, it's deployed to a server to run on its own — no longer a manual, one-time campaign push.
- Schneider closes by promoting [[entities/graphed|Graphed.com]]'s "forward-deployed engineers" service: marketing agents implemented in 5 business days.

## Notable Quotes

> "GTM engineering today ... once the system works, deploy this to a server so it runs on its own."

## Entities Mentioned

- [[entities/cody-schneider|Cody Schneider]] — author
- [[entities/apify|Apify]] — scrapes competitor Facebook Ads Library creative
- [[entities/gemini|Gemini]] — describes ad images/video (angle, promise, outcome)
- [[entities/exa-ai|Exa AI]] — scrapes Reddit to validate ideated market gaps
- [[entities/nano-banana|Nano Banana]] — generates gap-filling ad creative (images)
- [[entities/seedance|Seedance]] — generates gap-filling ad creative (video)
- [[entities/graphed|Graphed]] — MCP-connected performance analysis; also promoted at the end as a 5-day forward-deployed marketing-agent implementation service

## Concepts Touched

- [[concepts/competitor-creative-gap-analysis|Competitor Creative Gap Analysis]] — the concept this post introduces
- [[concepts/ai-ugc-ads|AI UGC Ads]] — the sibling pipeline this extends: research source shifts from Reddit-pain-points-first to competitor-creative-first, with Reddit demoted to a validation step
- [[concepts/ad-library-market-validation|Ad Library Market Validation]] — same raw data source (Facebook Ads Library) used for a different purpose: mapping category messaging to find a gap, not validating a product idea before building
- [[concepts/gtm-agents|GTM Agents]] — the autonomous, server-deployed closed loop is a direct instance of this concept

## My Notes

Extremely terse even by Schneider's standard — no numbers at all this time (no CTR, no CPM, no revenue figure), which is unusual for his threads and worth flagging: every other Schneider source in this wiki anchors its claims with at least one metric. Treat the entire pipeline as an unverified, single-source method description. The genuinely new piece relative to prior wiki content is the *research input*: previous Schneider ad pipelines start from the advertiser's own customer pain (Reddit, sales transcripts). This one starts from what competitors are already claiming and searches for the unclaimed space — a market-structure approach rather than a customer-pain approach, reconciled with Reddit only as a validation step afterward, not the primary source.

## See Also

- [[sources/codyschneider-ai-ugc-ads]] — the original Reddit-first UGC ad pipeline this post's method complements
- [[sources/codyschneider-fb-ads-ugc-playbook]] — prior detailed execution spec for the same broader Facebook ads system
- [[sources/theory-fb-ads-library-claude-saas]] — the wiki's other Facebook Ads Library method, used for product validation rather than creative gap-finding
- [[concepts/competitor-creative-gap-analysis]] — the synthesized concept page
- [[sources/codyschneider-gtm-agents]] — the original GTM agents stack this pipeline extends
