---
title: "PromptWatch"
type: entity
entity_kind: tool
tags: [tool, ai-search, seo, citations, intelligence]
created: 2026-06-16
updated: 2026-08-07
sources: [codyschneider-ai-search-seo, codyschneider-ai-citation-loop]
---

# PromptWatch

A tool for identifying which sources (citations) AI search platforms use when answering queries in a given category. Used in the [[AI Search SEO]] workflow to map the citation landscape before doing outreach, and — per its second, more detailed sourcing — to find specific prompt-level content gaps against named competitors.

## Role in This Wiki

The **citation intelligence layer** for AI search optimization. Before you can acquire citations, you need to know which sources AI search platforms are actually pulling from. PromptWatch surfaces this — the output is an exportable list of citations ranked by frequency and influence.

## Position in Stack (Original: Citation Acquisition)

```
Target keywords → PromptWatch (map which citations AI uses) → export + rank citations →
cold email site owners via Instantly → paid citation inclusion
```

## API Detail and Second Use Case (August 2026)

[[sources/codyschneider-ai-citation-loop]] names PromptWatch's API specifically, with more capability than the original source described: it returns every tracked prompt for a brand, who got cited in the answer **per model** (ChatGPT, Claude, Gemini, Perplexity, Grok), and **agent analytics** — which AI crawlers actually hit the operator's pages. The new technique this enables: pull two lists — prompts where the operator already shows up, and prompts where a named competitor shows up and the operator doesn't. The second list becomes the content calendar for [[concepts/citation-shape-engineering|citation shape engineering]], a structurally different approach to citation acquisition than the original cold-email-for-placement method above (see that concept for the contrast).

## See Also

- [[sources/codyschneider-ai-search-seo]] — original source (citation-acquisition-by-outreach use case)
- [[sources/codyschneider-ai-citation-loop]] — second source (prompt-gap identification + agent-crawler analytics)
- [[concepts/ai-search-seo]] — the concept page; Lever 2 (citation acquisition) depends on PromptWatch
- [[concepts/citation-shape-engineering]] — the newer pipeline PromptWatch's gap-list technique feeds
- [[entities/instantly]] — the cold email tool used to reach citation site owners in the original use case
- [[entities/dataforseo]] — downstream step in the newer pipeline; sizes the gaps PromptWatch identifies
