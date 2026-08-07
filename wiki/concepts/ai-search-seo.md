---
title: "AI Search SEO"
type: concept
tags: [seo, ai-search, aio, citations, content-marketing, organic]
created: 2026-06-16
updated: 2026-08-07
sources: [codyschneider-ai-search-seo, codyschneider-seo-for-saas-101, codyschneider-ai-citation-loop]
---

# AI Search SEO

The practice of optimizing for visibility in AI-generated search answers (ChatGPT, Perplexity, Claude, etc.) rather than traditional blue-link SERPs. [[Cody Schneider]]'s framing: **AI search is not a new discipline — it is SEO with two levers.**

## The Core Reframe

AI search doesn't change what works. It changes where results appear. The inputs are the same: rank where your audience searches, then be cited by the sources those searches trust. Tactics invented specifically for "AI SEO" (prompt stuffing, AI content farms, etc.) are mostly noise. The signal is traditional SEO combined with citation acquisition.

## The Two Levers

### Lever 1: Rank Page 1–3 for Bottom-of-Funnel Keywords

AI search platforms pull referral traffic from pages ranking on page 1–3 for high-intent queries. The keyword patterns that matter:

| Pattern | Example |
|---------|---------|
| Best X for Y | "best CRM for agencies" |
| X alternative | "Salesforce alternative" |
| Tools like X | "tools like Airtable" |
| Better than X | "better than HubSpot" |
| Apps like X | "apps like Notion" |

**The process:**
1. Scrape page 1 rankings for target patterns
2. Define product differentiation vs. what ranked
3. Write a post that includes your product, how it differs, and who it's for
4. Publish and add to sitemap
5. Optimize page speed (crawl budget signal)

This is standard SEO. The AI search amplifier: when AI surfaces an answer to "best X for Y," it pulls from these ranked pages — so ranking = citation in AI answers.

**Named-tool version (July 2026):** [[sources/codyschneider-seo-for-saas-101]] restates this same process with specific tools and two additions. Keyword discovery runs through Claude Code against an SEO data API rather than manual research; page-1 scraping runs through [[entities/serper|Serper]]. The new step: rather than writing the article from competitor-ranking content alone, the founder records a 30-minute video (or is interviewed by the Claude mobile app) giving their own perspective on the industry, and the article is written from ranking research *plus* that perspective. See [[concepts/founder-perspective-content-moat]] for why this step, not the mechanical ones, is argued to be the actual differentiator. Conversion instrumentation is also more specific here: CTA injected after the first paragraph and at 25/50/75% scroll depth, tracked via Google Tag Manager + Google Analytics 4 + Google Search Console together.

### Lever 2: Get Cited by Sources AI Search Already Trusts

AI search platforms don't discover new sources — they pull from sources that already have authority in a category. Getting onto those sources is the faster path to AI citation than building new authority from scratch.

**The process:**
1. Identify which citations AI search uses for your category keywords — use [[PromptWatch]] to map this
2. Export the citation list; rank by citation frequency (not all citations are equal)
3. Find emails of site owners / article writers
4. Cold email asking for inclusion (via [[Instantly]]); expect paid placement
5. Prioritize: pay more for high-frequency citations, less for the long tail

**The priority-stacking insight:** In any category, a small number of sources dominate citation frequency. Getting onto those sources creates disproportionate AI search presence. Map the full citation landscape first, then allocate budget by citation weight.

**A structural alternative (August 2026):** [[sources/codyschneider-ai-citation-loop]] describes a fundamentally different route to the same goal — instead of buying placement on someone else's already-cited page, reverse-engineer the *structural shape* of what gets cited and rewrite your own content to match it directly. The claim: LLM retrieval operates on chunks, not whole pages, so a page built from independently-answering 200–400 word sections (each front-loaded with a 40-word answer, literal-question H2s, named-competitor comparison tables, and FAQPage + Article schema) gets cited on its own merits, no outreach required. See [[concepts/citation-shape-engineering]] for the full technique. This doesn't strictly contradict the outreach-based Lever 2 above — an operator could run both — but it is a genuinely different theory of what makes citation acquirable (bought placement vs. earned structure), and the two sources don't reconcile or reference each other.

## Technical Amplifiers

| Factor | What It Does |
|--------|-------------|
| **Sitemap density** | 100 pages per sitemap URL speeds up indexing for large sites |
| **Page size** | Extremely small pages → more crawl budget → faster and deeper indexing |
| **Keyword-H1 match** | Same principle as the paid ads playbook: page H1/P1 = target keyword |

## Connection to GTM Agents

The SEO agent in [[GTM Agents]] executes Lever 1 autonomously:
- [[Ahrefs]] MCP for keyword research
- CMS API for publishing
- Sitemap management
- [[PostHog]] for performance tracking

Lever 2 (citation acquisition) requires a semi-manual campaign — but [[Instantly]] is already part of the GTM stack, so it maps cleanly to the cold outreach agent with a different target list (site owners vs. prospects).

## Relationship to Paid Ads

| Dimension | AI Search SEO (Lever 1) | Paid Ads (Google) |
|-----------|------------------------|------------------|
| Intent targeting | Same keyword patterns | Same keyword patterns |
| Landing page | H1/P1 = keyword | H1/P1 = keyword |
| Conversion tracking | Site analytics | Signup + payment events |
| Speed | Slow (organic, weeks/months) | Fast (immediate traffic) |

Both levers produce the same keyword-match principle. See [[sources/codyschneider-paid-ads-playbook]] for the paid version of the same logic.

## Open Questions

- How frequently do AI search citation sources rotate? A site with authority today may be deprioritized as platforms update their retrieval models. [low confidence on stability]
- Does PromptWatch cover all major AI search platforms (ChatGPT, Perplexity, Claude, Gemini) or only some? [unknown from source]
- Is paid citation placement (paying site owners for inclusion) a durable tactic or a race to the bottom as more SaaS companies adopt this? [unknown]
- Given both an outreach-based route (Lever 2 above) and a structure-based route ([[concepts/citation-shape-engineering]]) now exist in this wiki from the same author with no cross-reference between them, which does Schneider actually consider primary — or are they meant as complementary, sequential layers he simply hasn't written up together yet? [unresolved]

## Related: Content-Type Durability (Harries)

[[concepts/seo-mini-tools]] (from [[sources/lukeharries-elevenlabs-growth-playbook]]) adds a durability layer underneath this framework's discovery mechanics: long-form blog content is expected to decline as AI answers absorb query volume, but single-purpose, engineered mini-tools embedded in a page (e.g., a working text-to-speech box that ranks for "text to speech Spanish") should keep working for years, because they require real product engineering, not just words, so an LLM can't casually replicate or replace them as a search result. Consistent with but distinct from this page's Lever 1 (rank for comparison keywords) — that lever is about *which pages* to build; the mini-tools thesis is about *what kind* of page survives the shift.

## See Also

- [[sources/codyschneider-ai-search-seo]] — the primary source
- [[sources/codyschneider-seo-for-saas-101]] — named-tool version of Lever 1 with the founder-perspective addition
- [[sources/codyschneider-ai-citation-loop]] — structural alternative to Lever 2's outreach-based citation acquisition
- [[concepts/founder-perspective-content-moat]] — durability layer this later post adds to Lever 1
- [[concepts/citation-shape-engineering]] — structural alternative to Lever 2's citation-acquisition approach
- [[entities/promptwatch]] — the citation intelligence tool
- [[concepts/gtm-agents]] — the SEO agent that executes Lever 1 autonomously
- [[sources/codyschneider-gtm-agents]] — the original SEO agent blueprint
- [[sources/codyschneider-paid-ads-playbook]] — same simplicity framing; keyword-matching principle applies across SEO and paid
- [[concepts/seo-mini-tools]] — content-type durability thesis; the "two pages" survive-AI-search argument
- [[concepts/directory-website-seo-play]] — Schneider's own directory-site tactic, indexed via Google Search Console; a property-scale application of this concept's Lever 1
