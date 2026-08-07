---
title: "Right Now You Can Make a Media Company That Promotes Your Business"
type: source
tags: [ai-agents, content-marketing, media-company, directory-website, podcast, tiktok, cody-schneider]
created: 2026-07-17
updated: 2026-07-17
sources: [codyschneider-ai-media-company-playbook]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2078102503363694744"
source_type: other
---

# Right Now You Can Make a Media Company That Promotes Your Business

**Author:** [[entities/cody-schneider|Cody Schneider]]
**Date:** 2026-07-17
**Source:** [x.com/codyschneider/status/2078102503363694744](https://x.com/codyschneider/status/2078102503363694744)

## Core Thesis

A business can run its own media company as a promotion channel, built and operated entirely by AI agents on top of Claude Code or Codex. Schneider names three concrete instances he is running: a niche directory website, an industry news podcast paired with an email newsletter, and a TikTok "reel farm." Each is a distinct audience-acquisition surface that terminates in ads for his own product — the media property is not the business, it is the funnel.

## Key Points

- **Directory website:** a [[entities/hermes-agent|Hermes agent]] scrapes and researches every company in the target industry. Claude Code, in plan mode, designs the directory site around that dataset, then builds the whole site in one pass in auto mode (~30 minutes). Publish via [[entities/vercel|Vercel]], index via [[entities/google-search-console|Google Search Console]], and refresh monthly using content-gap analysis against Search Console data. Schneider cites one directory site, built 90 days prior, doing 100 clicks/day — used as an ad placement for his own product.
- **Podcast + newsletter:** an agent researches fast-growing businesses in the industry, mining podcast interviews as the primary source on *how* they grew. The agent writes a 10-minute monologue script, [[entities/elevenlabs|ElevenLabs]] reads it as audio, and the MP3 is hosted on [[entities/transistor-fm|Transistor.fm]]. A companion email newsletter is built and prompted toward the target audience — Schneider reports growing a list to 20K in 6 months — with ads run inside the newsletter itself.
- **TikTok reel farm:** [[entities/doublespeed-ai|DoubleSpeed AI]] creates TikTok accounts in the cloud; [[entities/nano-banana|Nano Banana]] generates slideshow images following viral formats, with the product mentioned inside the slides. A 10-account cohort produces ~300K aggregate impressions at roughly $3 CPM.
- All three pipelines are described as "entirely run by agents" — the human role is prompting, plan-mode direction, and monitoring, not manual production.

## Notable Quotes

> "Right now you can make a media company that promotes your business powered by AI agents."

## Entities Mentioned

- [[entities/cody-schneider|Cody Schneider]] — author
- [[entities/hermes-agent|Hermes Agent]] — scraping/research agent for the directory dataset
- [[entities/vercel|Vercel]] — hosting/publishing for the directory site
- [[entities/google-search-console|Google Search Console]] — indexing and content-gap data source
- [[entities/elevenlabs|ElevenLabs]] — text-to-speech for the podcast monologue
- [[entities/transistor-fm|Transistor.fm]] — podcast MP3 hosting
- [[entities/doublespeed-ai|DoubleSpeed AI]] — cloud TikTok account creation
- [[entities/nano-banana|Nano Banana]] — AI slideshow image generation

## Concepts Touched

- [[concepts/ai-media-company-playbook|AI Media Company Playbook]] — the umbrella thesis this post introduces
- [[concepts/directory-website-seo-play|Directory Website SEO Play]] — tactic 1, detailed
- [[concepts/podcast-newsletter-growth-loop|Podcast + Newsletter Growth Loop]] — tactic 2, detailed
- [[concepts/tiktok-reel-farm|TikTok Reel Farm]] — tactic 3, detailed
- [[concepts/gtm-agents|GTM Agents]] — all three tactics are instances of the broader agents-run-GTM-work thesis
- [[concepts/seo-mini-tools|SEO Mini-Tools]] — adjacent durable-content thesis; directory sites and mini-tools are both "engineered" content Schneider treats as more defensible than blog posts

## My Notes

Terse compared to Schneider's usual long-form posts — no numbers behind the 100 clicks/day or 20K list beyond the headline figures, and no detail on directory-site monetization mechanics beyond "run ads on it." Treat the specific metrics as [low confidence] single-source claims. The post is notable mainly for reframing prior wiki concepts ([[concepts/seo-mini-tools]], [[concepts/ai-search-seo]], [[concepts/gtm-agents]]) as pieces of a broader "become a media company" strategy rather than isolated SEO/ads tactics.

## See Also

- [[entities/cody-schneider]] — author; prior sources in this wiki
- [[concepts/ai-media-company-playbook]] — the synthesized concept page
- [[concepts/seo-mini-tools]] — related durable-content thesis (ElevenLabs case)
- [[concepts/ai-search-seo]] — directory site indexing overlaps with this concept's Lever 1
- [[sources/codyschneider-gtm-agents]] — the original GTM agents stack this playbook extends
