---
title: "SEO for SaaS 101"
type: source
tags: [seo, ai-search, content-marketing, cody-schneider, gtm-agents]
created: 2026-07-28
updated: 2026-07-28
sources: [codyschneider-seo-for-saas-101]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2081831994808205503"
source_type: other
---

# SEO for SaaS 101

**Author:** [[entities/cody-schneider|Cody Schneider]]
**Date:** 2026-07-27
**Source:** [x.com/codyschneider/status/2081831994808205503](https://x.com/codyschneider/status/2081831994808205503)

## Core Thesis

A more concrete, tool-specific execution spec for the SEO agent's Lever 1 (rank for bottom-of-funnel keywords) already in the wiki, with one genuinely new element: instead of writing the article from competitor-ranking content alone, the founder records a 30-minute video (or is interviewed by the Claude mobile app) giving their actual perspective on the industry, and that perspective is folded into the article alongside the competitive research. The top comment on the post names this the actual differentiator: once everyone runs the mechanical version of this playbook, the ranked article becomes a commodity — the perspective a model can't synthesize from the other nine ranking pages is what survives.

## Key Points

- **Keyword discovery:** use Claude Code with an SEO data API to find bottom-of-funnel keywords related to the product — same patterns as the wiki's existing [[concepts/ai-search-seo|AI Search SEO]] Lever 1 (x vs. y, competitor x alternative, x review, best x for y).
- **Competitive research:** for each target keyword, scrape what's currently ranking on page 1 using [[entities/serper|Serper]].
- **Perspective input:** put the ranking content in context, then record a 30-minute video giving your own perspective on the industry — or have the Claude mobile app interview you instead of writing the video yourself.
- **Article generation:** for each keyword, write the article from what's ranking *plus* the recorded perspective — not from competitor content alone.
- **Publish:** push the article to the CMS via API.
- **Conversion instrumentation:** inject a CTA after the first paragraph and at 25%, 50%, and 75% scroll depth.
- **Tracking:** track the conversion event against the specific landing page using Google Tag Manager, Google Analytics 4, and [[entities/google-search-console|Google Search Console]] together.
- **Feedback loop:** publish more content modeled on whatever performs best.
- **Reporting:** build a dashboard for SEO and AI-search referral traffic.
- Closes with the same [[entities/graphed|Graphed.com]] "forward-deployed engineers, 5 business days" promotion seen in the prior Schneider post in this wiki.

## Notable Quotes

> "for each keyword write article based on what is ranking + perpective" [sic]

## Entities Mentioned

- [[entities/cody-schneider|Cody Schneider]] — author
- [[entities/serper|Serper]] — SERP scraping API for competitive research
- [[entities/google-search-console|Google Search Console]] — part of the conversion-tracking stack
- [[entities/graphed|Graphed]] — promoted at the end as a 5-day marketing-agent implementation service

## Concepts Touched

- [[concepts/ai-search-seo|AI Search SEO]] — the concept this post extends with a more concrete tactical spec for Lever 1
- [[concepts/founder-perspective-content-moat|Founder Perspective Content Moat]] — the concept this post introduces
- [[concepts/founder-brand-strategy|Founder Brand Strategy]] — convergent principle from a different domain (Harries/ElevenLabs): channel-fit and authenticity as the moat, here applied specifically to SEO content
- [[concepts/gtm-agents|GTM Agents]] — this is an updated tactical spec for the SEO agent already named in that concept

## My Notes

The interview/video step is the one piece of this post genuinely absent from the wiki's existing SEO tactical spec — everything else (keyword patterns, scrape-page-1, publish-via-API, remix-the-winners) restates [[sources/codyschneider-ai-search-seo]] with different tool names (Serper instead of unspecified scraping, Claude Code + an SEO API instead of manual keyword research). Worth flagging: an X commenter (@TheDistroGuy) makes the sharpest observation in the thread — "the moat is buried in step 5: the 30-min POV clip... content scales, taste doesn't" — which is a more precise statement of the post's actual thesis than anything Schneider wrote directly. Treated here as an interpretive lens on the source, not as an additional primary claim from Schneider himself. No metrics or results are given anywhere in this post, consistent with [[sources/codyschneider-ad-library-gap-analysis]] (the prior Schneider ingest) — treat the whole spec as directional.

## See Also

- [[sources/codyschneider-ai-search-seo]] — the original Lever 1/Lever 2 framework this post re-executes with named tools
- [[sources/lukeharries-elevenlabs-growth-playbook]] — source of the wiki's other founder-authenticity-as-moat argument
- [[sources/codyschneider-transcript-personas]] — the wiki's other interview/transcript-mining technique, there for ad personas rather than SEO articles
- [[concepts/founder-perspective-content-moat]] — the synthesized concept page
- [[sources/codyschneider-gtm-agents]] — the original GTM agents stack this SEO agent spec extends
