---
title: "SEO Mini-Tools ('Two Pages')"
type: concept
tags: [seo, mini-tools, ai-search, product-led-growth, enterprise-trial]
created: 2026-07-15
updated: 2026-07-15
sources: [lukeharries-elevenlabs-growth-playbook]
---

# SEO Mini-Tools ("Two Pages")

*The thesis that classic long-form blog SEO is fading, but single-purpose, engineered mini-tools embedded in a page will keep working as an SEO and trial asset for years, because LLMs can't trivially replicate them.*

## Overview

[[entities/luke-harries|Luke Harries]]' framing: long-form blog content ("the first one... long words, long-form articles") is expected to decline as AI answer engines absorb more query volume directly — though it isn't dead yet (Zapier still gets 70%+ of its SEO traffic from blog content, per the source). What he's confident survives at least ~5 years is the second category: **"two pages"** — pages built around a working mini-tool (his example: searching "text to speech Spanish" surfaces ElevenLabs' own text box where a visitor can type Spanish text, pick a voice, and hear it played back). The durability argument: this requires real product engineering to exist, not just words, so an LLM can't casually out-produce or replace it as a search result — and by the time an LLM *can* spin up an equivalent tool dynamically on the fly, it's effectively already delivering your product's value directly, which is a different (and arguably favorable) competitive position, not a loss.

This connects to and extends the wiki's existing [[concepts/ai-search-seo]] concept (Cody Schneider's two-lever framework: rank for comparison keywords + acquire AI citations). Where Schneider's framework addresses *how to get discovered* in an AI-search world, Harries' mini-tool thesis addresses *what kind of content survives being discovered* — a durability layer underneath the discovery mechanics.

## Key Properties / Characteristics

- Two SEO content types, with diverging trajectories: long-form blog (declining, not dead) vs. embedded mini-tools (durable).
- Mini-tools require actual engineering investment — this is the moat, not the words on the page.
- The same underlying capability (small, self-contained slices of product value, exposed outside any login wall) doubles as the fix for a completely separate problem: proving value to enterprise buyers who won't commit without trying something.

## How It Works

**As an SEO asset:** build a narrow, single-purpose tool around a specific high-intent search query (e.g., "text to speech Spanish"), embed it directly on a page with no signup required, and let it rank on its own utility. ElevenLabs' homepage is described as being built almost entirely from a cluster of these free-to-try text boxes across its different products (text-to-speech, speech-to-text, etc.), all outside the login wall.

**As an enterprise-trial asset:** the same construction solves a distinct problem — enterprise buyers won't buy without trying the product, but a company can't give away its entire enterprise offering for free. The growth engineer's job (see [[concepts/growth-hiring-order]], hire #2) is to expose small, genuinely valuable slices of the product — enough to produce a "wow moment" fast — without exposing the whole product.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/lukeharries-elevenlabs-growth-playbook]] | Zapier still gets 70%+ of its SEO traffic from blog-style content today | medium (cited as a known industry data point, not ElevenLabs' own data) |
| [[sources/lukeharries-elevenlabs-growth-playbook]] | ElevenLabs' text-to-speech mini-tool page ranks #1 for "text to speech Spanish" | medium (practitioner claim, not independently verified via search at time of ingest) |
| [[sources/lukeharries-elevenlabs-growth-playbook]] | AI chat usage share shifted from roughly 1.5 to 4.5 [units/metric unspecified in source] over six months, cited as evidence of accelerating query cannibalization from traditional search | low (the metric itself is ambiguous in the transcript — likely a reference to ChatGPT/AI search usage-share data cited by "Guillermo," but the specific figure and source aren't identifiable from the transcript alone) |

## Contradictions & Open Questions

- The claim that LLM-generated dynamic pages won't threaten mini-tools "for a while" is asserted, not defended with a mechanism — worth treating as directional opinion rather than a technical forecast.
- Open question: does this thesis apply equally to mini-tools built on top of proprietary data/models (ElevenLabs' case) versus mini-tools that are thin wrappers around a commodity LLM call? The source's confidence seems implicitly tied to the former.

## See Also

- [[concepts/ai-search-seo]] — the existing wiki concept this extends; two-lever discovery framework vs. this page's durability-of-content-type framework
- [[concepts/launch-playbook]] — blog posts are one of the fixed launch assets; this concept explains why the blog *and* a mini-tool are often built together
- [[concepts/growth-hiring-order]] — the growth engineer is the hire responsible for building these tools
- [[concepts/directory-website-seo-play]] — a related engineered-content durability play: a scraped-data directory site rather than a single interactive tool
- [[concepts/founder-perspective-content-moat]] — a third durability variant: personal, un-synthesizable perspective rather than engineering effort, as the moat against AI replication
- [[sources/lukeharries-elevenlabs-growth-playbook]] — primary source
