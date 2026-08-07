---
title: "Citation Shape Engineering"
type: concept
tags: [ai-search, citations, seo, structured-data, content-marketing]
created: 2026-08-07
updated: 2026-08-07
sources: [codyschneider-ai-citation-loop]
---

# Citation Shape Engineering

*Reverse-engineer the structural shape of content that already gets cited by AI answer engines, then mechanically rewrite your own content into that exact shape at scale with a coding agent — because models retrieve chunks, not pages.*

## Overview

[[entities/cody-schneider|Cody Schneider]]'s core claim: getting cited by AI search models has nothing to do with writing quality and everything to do with structure. Fetch the top-cited URLs for the prompts you're losing, and what they share isn't better prose — it's a specific, repeatable shape: the answer stated in the first 40 words, headings phrased as the literal question a user typed, comparison tables naming competitors, numbers and dates co-located with the claims they support, and self-contained 200–400 word sections. The mechanism this shape is optimized for: **LLM retrieval operates on chunks, not whole pages.** A long essay with the real answer buried deep never surfaces, because nothing retrievable maps cleanly onto the query. A page built from independently-answering sections gets pulled into multiple different answers because each section is itself a viable retrieval unit.

This reframes the wiki's existing [[concepts/ai-search-seo|AI Search SEO]] Lever 2 (citation acquisition). The prior approach treated citation as something purchased: map which sites AI models already cite, then cold-email those site owners for paid inclusion. This concept treats citation as something *earned structurally*: don't try to get onto someone else's authoritative page — restructure your own page so it retrieves the same way an already-cited page does. The two approaches aren't strictly incompatible (a operator could run both), but they represent genuinely different theories of what makes AI search citation acquirable, and the wiki now holds both.

The concept also sits in direct tension with [[concepts/founder-perspective-content-moat]], introduced from a Schneider post roughly ten days earlier. That concept argued the durable input, once a content pipeline's mechanical steps are commoditized, is a founder's personal, non-synthesizable perspective. This concept argues the opposite emphasis in the same breath: what gets cited is pure structure — a mechanical shape any agent can reproduce from public citation data, with no personal perspective step anywhere in the six-step loop. Read together, they represent an unresolved disagreement (or at least an unreconciled emphasis shift) within Schneider's own output about what actually differentiates AI-search-optimized content.

## Key Properties / Characteristics

- The unit of retrieval is the chunk/section, not the page — content must be structured so any individual section can stand alone as a complete answer.
- Named structural features, all falsifiable and checkable: front-loaded 40-word answers, literal-question H2s, named-competitor comparison tables, number+date co-location with claims, 200–400 word section length, repeated brand/category-term proximity.
- Structured data (FAQPage + Article schema) is an explicit requirement in the write step, not an optional enhancement.
- The research step (fetch and analyze top-cited URLs) happens before any writing — the shape is derived empirically from what's already working in the category, not designed from theory.
- Measurement is citation-array membership on a re-run of the same prompts, not traditional rank position — a fundamentally different success metric from classical SEO.

## How It Works

1. Pull prompts where a competitor is cited and the operator isn't, via [[entities/promptwatch|PromptWatch]]'s per-model citation API.
2. Size each opportunity via [[entities/dataforseo|DataForSEO]]'s AI Optimization API (search volume inside AI tools, mention counts vs. competitors, live full-answer + citation data across ChatGPT/Claude/Gemini/Perplexity for the same prompt).
3. Fetch the top 20 cited URLs for the target prompts and have an agent extract their structural commonalities — not content, structure.
4. Have a coding agent write new content matching that shape: 40-word front-loaded answer, competitor H2 questions as the outline, comparison table, FAQPage + Article schema, output as CMS-ready JSON.
5. Publish the batch directly via the CMS API (Strapi/WordPress/Ghost/Webflow), then submit via IndexNow and Search Console.
6. Re-run the same prompt queries two weeks later; check citation-array membership, not ranking.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/codyschneider-ai-citation-loop]] | The six named structural features are what top-cited URLs across a category consistently share | low (asserted from Schneider's own described analysis process; no independent verification, no named example category or URLs) |
| [[sources/codyschneider-ai-citation-loop]] | DataForSEO's AI Optimization API calls cost "pennies," contrasted with a "$500/month seat" AI-visibility dashboard | low (no product named for comparison, no actual DataForSEO pricing cited) |

## Contradictions & Open Questions

- Directly in tension with [[concepts/founder-perspective-content-moat]] (same author, ~10 days earlier): that post's thesis is that personal perspective is the un-synthesizable moat once mechanics commoditize; this post's thesis is pure mechanical shape-matching with no perspective input at all. Neither post acknowledges the other. Worth treating as an open question about which Schneider actually believes matters more — or whether he sees them as complementary layers (structure gets you retrieved; perspective differentiates once you are) that this post simply doesn't address.
- No before/after citation results are given for any of Schneider's own properties — the entire method is asserted, not demonstrated with a specific case.
- "Have codex code fetch" — the post names a different coding agent (Codex) for the fetch/analyze step than the write step (explicitly Claude Code). Unclear whether this is a deliberate two-agent architecture or loose phrasing; captured as-stated. See [[entities/codex]].
- If citation shape becomes a widely-known, gameable structure (which this post itself publishes for a wide audience), the differentiation value could compress the same way [[concepts/founder-perspective-content-moat]] argues mechanical SEO steps already have — an unaddressed self-undermining risk in publishing the exact shape publicly.

## See Also

- [[sources/codyschneider-ai-citation-loop]] — primary source
- [[concepts/ai-search-seo]] — the base two-lever framework; this concept is a structural alternative to that framework's existing Lever 2
- [[concepts/founder-perspective-content-moat]] — unreconciled tension: personal perspective vs. pure structural mechanics as the differentiator
- [[concepts/gtm-agents]] — the broader autonomous-agent thesis this pipeline instantiates
- [[entities/promptwatch]], [[entities/dataforseo]], [[entities/codex]], [[entities/indexnow]] — the tool chain
