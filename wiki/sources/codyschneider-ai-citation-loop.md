---
title: "Half of Winning With AI Search Is Just Writing Content AI Wants to Consume"
type: source
tags: [ai-search, seo, citations, cody-schneider, gtm-agents, structured-data]
created: 2026-08-07
updated: 2026-08-07
sources: [codyschneider-ai-citation-loop]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2085395478154281432"
source_type: other
---

# Half of Winning With AI Search Is Just Writing Content AI Wants to Consume

**Author:** [[entities/cody-schneider|Cody Schneider]]
**Date:** 2026-08-06
**Source:** [x.com/codyschneider/status/2085395478154281432](https://x.com/codyschneider/status/2085395478154281432)

## Core Thesis

Getting cited by AI search models is not about buying placement on already-authoritative sites (the wiki's existing Lever 2 approach: map citations, then cold-email site owners for paid inclusion). It's about reverse-engineering the exact structural shape of content that already gets cited — because LLM-based answer engines retrieve chunks, not pages — and mechanically rewriting your own content into that shape at scale using a coding agent, then re-checking two weeks later whether you've entered the citation set. The most detailed, technically specific Schneider post in the wiki to date, and the first to name concrete API endpoints, structured-data requirements, and multiple named coding agents in the same pipeline.

## Key Points

- **Step 1 — Find the gap:** [[entities/promptwatch|PromptWatch]]'s API returns every tracked prompt for a brand, who got cited in the answer per model (ChatGPT, Claude, Gemini, Perplexity, Grok), and agent analytics showing which AI crawlers actually hit your pages. Pull two lists: prompts where you already show up, and prompts where a competitor shows up and you don't. The second list is the content calendar.
- **Step 2 — Size the opportunity:** [[entities/dataforseo|DataForSEO]]'s AI Optimization API. `ai_keyword_data/keywords_search_volume/live` gives search volume for how people phrase queries *inside* AI tools (longer, more conversational, different from Google phrasing). `llm_mentions/live` gives mention counts/impressions for a brand vs. competitors on a given keyword. The `llm_responses/live` endpoints (one per model: ChatGPT, Claude, Gemini, Perplexity) return the full answer text and every citation for the same prompt, live, across all four models — at "pennies per call," explicitly contrasted with a "$500/month seat" for an AI-visibility dashboard product.
- **Step 3 — Read the citations before writing:** take the top 20 cited URLs across the target prompts, have an agent (Schneider names "codex" specifically here) fetch all of them and identify what they structurally have in common. The finding: it's never "better writing" — it's shape. Answer in the first 40 words before any setup. H2 headings written as the literal question someone typed. A comparison table naming competitors. Specific numbers and dates in the same sentence as the claim they support. 200–400 word sections that stand alone. Brand name placed next to the category term repeatedly. The underlying mechanism: **models retrieve chunks, not pages** — a 3,000-word essay with the answer buried in paragraph 14 is never cited; a page where every section independently answers a question gets cited multiple different ways.
- **Step 4 — Write with a coding agent, not a chat window:** the post gives a literal agent prompt — read a prompts.json file, fetch every cited URL per prompt, extract heading structure and how the first paragraph answers the question, then write a post that answers the prompt in the first 40 words, uses competitors' H2 questions as the outline, includes a comparison table, and adds FAQPage + Article schema markup, output as JSON matching the operator's CMS schema. Schneider's stated reason it must be an agent, not a chat window: one run hits 4 APIs, fetches 20 pages, and writes 30 files.
- **Step 5 — Publish over the CMS API:** named endpoints for Strapi (`/api/articles`), WordPress (`/wp-json/wp/v2/posts`), Ghost (`/admin/api/posts`), and Webflow (flagged "(ew)" — the post's one aside). Give the agent an API token, POST the batch, then hit [[entities/indexnow|IndexNow]] and submit to Search Console. Push 20–30 posts in one command; never open the CMS admin UI.
- **Step 6 — Re-run in two weeks:** same `llm_responses` calls, same prompts. The metric is not ranking position — it's whether the URL now appears in the citations array. Schneider's closing claim: most people will spend the year buying an AI-visibility dashboard and never change a single page. The dashboard isn't the work; rewriting content into the shape models actually retrieve is the work.
- Promotes [[entities/graphed|Graphed]]'s CLI as the packaged version of this system, newly positioned (relative to prior Schneider posts) as deploying paid ads, cold outbound, *and* SEO agents together, backed by a data pipeline, data warehouse, and cloud server.

## Notable Quotes

> "models retrieve chunks, not pages"

> "the dashboard isn't the work / rewriting your content into the shape models actually retrieve is the work"

## Entities Mentioned

- [[entities/cody-schneider|Cody Schneider]] — author
- [[entities/promptwatch|PromptWatch]] — prompt-gap and per-model citation tracking, plus agent-crawler analytics
- [[entities/dataforseo|DataForSEO]] — AI Optimization API: search volume, mention counts, live LLM responses + citations across 4 models
- [[entities/codex|Codex]] — fetches and analyzes the top-cited URLs for structural commonalities (distinct from the writing-agent role, which the post assigns to Claude Code)
- [[entities/indexnow|IndexNow]] — instant-indexing submission after publish
- [[entities/graphed|Graphed]] — promoted at the end, now positioned around a CLI that deploys paid ads, cold outbound, and SEO agents together

## Concepts Touched

- [[concepts/citation-shape-engineering|Citation Shape Engineering]] — the concept this post introduces
- [[concepts/ai-search-seo|AI Search SEO]] — this post is effectively a full replacement for the wiki's existing Lever 2 (citation acquisition via cold-email placement)
- [[concepts/founder-perspective-content-moat|Founder Perspective Content Moat]] — in tension with this post: that concept argues personal, un-synthesizable perspective is the durable input; this post argues pure structural/mechanical shape-matching is what gets cited, with no mention of perspective at all
- [[concepts/gtm-agents|GTM Agents]] — a third, more technically detailed SEO agent spec added to that concept's growing pipeline list

## My Notes

Markedly more technically dense than the two prior Schneider posts in the wiki (both of which had zero supporting metrics or API-level detail) — this one names specific endpoint paths, gives a literal agent prompt, and quantifies cost ("pennies per call"). Still gives no before/after citation results for Schneider's own properties, so treat the method as directional despite the added specificity. Two things worth flagging explicitly: (1) this is the first source in the wiki where Schneider names a coding agent other than Claude Code — "codex" for the fetch-and-analyze step, Claude Code for the write step — which may just be looseness in the post's phrasing rather than a deliberate two-agent architecture, but is captured as stated; (2) the "models retrieve chunks, not pages" framing directly and usefully sharpens the wiki's existing citation-acquisition concept, which previously treated citation as something you buy rather than something you structurally earn.

## See Also

- [[sources/codyschneider-ai-search-seo]] — the original Lever 1/Lever 2 framework this post effectively rewrites Lever 2 of
- [[sources/codyschneider-seo-for-saas-101]] — the prior Schneider ingest (10 days earlier), whose founder-perspective durability argument this post's pure-mechanics approach sits in tension with
- [[concepts/citation-shape-engineering]] — the synthesized concept page
- [[sources/codyschneider-gtm-agents]] — the original GTM agents stack this SEO agent spec extends
