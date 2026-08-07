---
title: "Directory Website SEO Play"
type: concept
tags: [seo, directory-website, ai-agents, gtm-agents, ads]
created: 2026-07-17
updated: 2026-07-17
sources: [codyschneider-ai-media-company-playbook]
---

# Directory Website SEO Play

*Scrape every company in a target industry into a dataset, have an agent one-shot a directory website around it, then advertise your own product on the traffic it earns.*

## Overview

The first of [[entities/cody-schneider|Cody Schneider]]'s three [[concepts/ai-media-company-playbook|AI media company]] tactics. The directory functions as a niche SEO property built explicitly to attract the operator's own prospective customers (companies searching for or being searched for within their industry), monetized not by the directory itself but by ads placed on it for the operator's actual product. The build is framed as almost entirely agent-executed: a [[entities/hermes-agent|Hermes agent]] handles data collection, and Claude Code handles site planning and construction in a single working session.

This is a variant of the wiki's existing durable-content thesis ([[concepts/seo-mini-tools]]): both argue that engineered, data-backed pages outcompete written content because they require real work to reproduce. A directory site differs from a mini-tool in scope — it's a full dataset-backed property (many pages, one per listed company) rather than a single interactive utility.

## Key Properties / Characteristics

- Dataset-first: the scraped company research is the raw material the site is built around, not an afterthought.
- One-shot build claim: Claude Code in auto mode builds the entire site in ~30 minutes after plan-mode design.
- Living asset: refreshed monthly via content-gap analysis against Search Console data, not a static one-time build.
- Distribution is organic SEO (indexed via Search Console) plus paid — ads for the operator's product run directly on the directory site's traffic.

## How It Works

1. A [[entities/hermes-agent|Hermes agent]] scrapes and researches every company in the target industry (the specific dataset fields collected aren't detailed in the source).
2. Claude Code, in plan mode, is given the dataset and designs a directory site structure around it.
3. Claude Code, in auto mode, builds the full site in one pass — Schneider cites ~30 minutes.
4. The site is published via [[entities/vercel|Vercel]] and submitted for indexing via [[entities/google-search-console|Google Search Console]].
5. Monthly: content-gap analysis against Search Console query data drives a refresh of the site's content/pages.
6. Ads for the operator's own product run on the directory site.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/codyschneider-ai-media-company-playbook]] | A directory site built 90 days prior does 100 clicks/day | low (single-source, no traffic-source breakdown given) |

## Contradictions & Open Questions

- No detail on what "every company you're trying to sell to" actually populates on each listing page, or how listings are kept accurate as scraped companies change.
- 100 clicks/day is a modest number for a claimed working SEO channel — unclear if this is early-stage growth or a ceiling.
- Ad mechanics on the directory site (self-hosted banner vs. ad network vs. manual placement) are unspecified.

## See Also

- [[concepts/ai-media-company-playbook]] — parent concept; the other two tactics
- [[concepts/seo-mini-tools]] — related durable, engineered-content thesis
- [[concepts/ai-search-seo]] — Lever 1 (rank for comparison/industry keywords) overlaps with directory-site indexing strategy
- [[entities/hermes-agent]] — the scraping/research agent
- [[entities/vercel]] — publishing platform
- [[entities/google-search-console]] — indexing and content-gap data source
- [[sources/codyschneider-ai-media-company-playbook]] — primary source
