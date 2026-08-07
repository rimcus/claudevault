---
title: "Stop Overcomplicating This: AI Search Is Just SEO"
type: source
tags: [seo, ai-search, aio, citations, content-marketing, gtm-agents]
created: 2026-06-16
updated: 2026-06-16
sources: [codyschneider-ai-search-seo]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2066657096091811885"
source_type: x-post
---

# Stop Overcomplicating This: AI Search Is Just SEO

**Author:** [[Cody Schneider]] (@codyschneider)
**Published:** 2026-06-16
**Context:** Short prescriptive post on AI search optimization. Companion to [[sources/codyschneider-paid-ads-playbook]] — same simplicity-first framing applied to organic/AI search. Promotes [[Graphed]] at the end.

---

## Core Thesis

AI search is not a new discipline. It is SEO with two levers instead of ten. Practitioners overcomplicating it are optimizing for things that don't matter. The only things that move the needle:

1. **Rank on page 1–3** for bottom-of-funnel keywords → AI search pulls referral traffic from those pages
2. **Get cited by sources AI search already trusts** → become a named citation in AI-generated answers

---

## Lever 1: Publish for Bottom-of-Funnel Keywords

**Target keyword patterns:**
- "best [X] for [Y]"
- "[X] alternative"
- "tools like [X]"
- "better than [X]"
- "apps like [X]"

**Process:**
1. Scrape what is currently ranking page 1 for these keywords
2. Define your product's differentiation vs. what ranked
3. Write a blog post that includes your product and specifically how it is different and who it is for
4. Publish the article and make sure it's added to the sitemap for indexing

**Pro tips:**
- **Sitemap:** if the site has a large number of posts, use 100 pages per sitemap URL — this makes indexing faster
- **Page speed:** make the page extremely fast (small file size) to increase crawl budget

---

## Lever 2: Get Mentioned on Existing AI Citations

AI search platforms (ChatGPT, Perplexity, Claude, etc.) pull from a specific set of citations when answering queries in a category. Getting onto those citation sources is the other side of the same coin.

**Process:**
1. Identify which citations AI search platforms are using for your target keywords — use [[PromptWatch]] for this
2. Export the full citation list
3. Find email addresses of site owners or individual article writers
4. Cold email them asking for citation inclusion (via [[Instantly]]) — expect to pay for placement
5. **Priority-stack citations:** map all citations in your category and rank by how frequently they are cited. Higher-cited sources warrant higher spend because they create higher impact faster.

**Pro tip:** Not all citations are equal. A few sources dominate citation frequency in each category. Pay more for those, less for the long tail.

---

## Why This Framing Matters

The "AI search is new" narrative leads practitioners to invent tactics that don't apply (prompt-stuffing, AI content farms, etc.) and ignore tactics that do (intent matching, citation authority, page speed). Schneider's reframe collapses both traditional SEO and AI search into the same two-lever system: rank where your audience searches, then ensure your name appears in the trusted sources those searches pull from.

Community confirms: *"at its core, it's about connecting intent with information, just like good old SEO. The fundamentals don't change."* — @NFTMansa

---

## Connection to GTM Agents

This post is the **tactical spec for the SEO agent** in Schneider's [[GTM Agents]] stack. The SEO agent listed in the original blueprint (landing pages 3/day, blog keyword → content → publish) is executing exactly this playbook:
- Lever 1 is the blog content loop (keyword research → write → publish → sitemap)
- Lever 2 (citation acquisition) is a manual/semi-automated campaign — this is where [[Instantly]] appears in the SEO context, not just cold outreach

---

## Entities Mentioned

- [[PromptWatch]] — tool for identifying which citations AI search platforms use
- [[Instantly]] — cold email platform; used here for citation outreach (not just lead gen)
- [[Graphed]] — promoted as the GTM agent implementation service

## Concepts Touched

- [[AI Search SEO]] — the two-lever framework this post defines
- [[GTM Agents]] — the SEO agent's tactical spec; citation acquisition as agent-executable workflow
- [[Cold Email Infrastructure]] — Instantly appears as citation outreach tool, not just lead gen

## See Also

- [[concepts/ai-search-seo]] — the concept page extracted from this method
- [[entities/promptwatch]] — the citation intelligence tool
- [[sources/codyschneider-paid-ads-playbook]] — same simplicity-first framing applied to paid ads
- [[sources/codyschneider-gtm-agents]] — the original blueprint where the SEO agent lives
- [[concepts/gtm-agents]] — SEO agent now has a tactical spec
