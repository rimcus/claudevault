---
title: "LLM Wiki Pattern"
type: source
tags: [llm, knowledge-management, obsidian, wiki, methodology]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern]
author: "Andrej Karpathy"
source_url: ""
source_type: article
---

# LLM Wiki Pattern

**Author:** [[Andrej Karpathy]]
**Date:** 2026-04-14
**Source type:** Gist / idea document

## Core Thesis

The key insight is that LLMs should not merely retrieve from raw documents at query time (RAG), but instead **incrementally build and maintain a persistent wiki** that sits between the user and the raw sources. Knowledge is compiled once and kept current, rather than re-derived on every query. This makes the knowledge base a compounding artifact: the more you add, the more valuable it becomes, because cross-references, contradictions, and synthesis are already in place.

## Key Points

- **RAG vs. Wiki:** RAG re-derives answers from scratch every query. An LLM-maintained wiki compiles knowledge incrementally — contradictions are flagged, cross-references are built, synthesis is preserved.
- **Three layers:** (1) Immutable raw sources, (2) LLM-maintained wiki, (3) Schema document (CLAUDE.md/AGENTS.md) that governs the LLM's behavior.
- **Human role:** Curate sources, ask good questions, direct analysis. LLM role: all the bookkeeping — summarizing, cross-referencing, maintaining consistency.
- **Toolchain:** Obsidian as the IDE for browsing; LLM as the programmer; the wiki as the codebase. The workflow is: LLM edits in real time while the user browses in Obsidian.
- **Operations:** Ingest (add a source → touch 5–15 pages), Query (answer → optionally file back into wiki), Lint (health-check for contradictions, orphans, gaps).
- **Index + Log:** Two navigation aids — `index.md` (content catalog, updated on ingest) and `log.md` (chronological append-only record, grep-parseable).
- **Why it works:** LLMs don't get bored doing maintenance. The cost of keeping the wiki current approaches zero, which is what causes humans to abandon wikis.
- **Historical resonance:** Related to Vannevar Bush's Memex (1945) — a private, curated knowledge store with associative trails. The Memex vision was closer to this than to the open web.

## Notable Quotes

> "The wiki is a persistent, compounding artifact. The cross-references are already there. The contradictions have already been flagged. The synthesis already reflects everything you've read."

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

> "Humans abandon wikis because the maintenance burden grows faster than the value. LLMs don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass."

## Entities Mentioned

- [[Andrej Karpathy]] — author, originator of this pattern
- [[Obsidian]] — recommended tool for browsing the wiki (the "IDE")
- [[qmd]] — recommended local search engine for markdown (BM25/vector hybrid)
- [[Vannevar Bush]] — historical precedent; creator of the Memex concept
- [[Marp]] — markdown slide deck format, Obsidian plugin
- [[Dataview]] — Obsidian plugin for querying frontmatter

## Concepts Touched

- [[LLM-Maintained Wiki]] — the core concept being defined
- [[Retrieval-Augmented Generation]] — the contrasting approach; what this pattern improves upon
- [[Memex]] — 1945 predecessor concept by Vannevar Bush
- [[Knowledge Compounding]] — the key value proposition: the wiki gets richer with each addition
- [[Schema-Governed LLM Behavior]] — using CLAUDE.md / AGENTS.md to make the LLM a disciplined maintainer

## My Notes

This is the founding document of this vault. The vault itself is an instantiation of the pattern described here. CLAUDE.md is the schema document Karpathy describes. This source page documents the meta-level: how this vault came to be and what philosophy it embodies.

The pattern is intentionally abstract — it describes the idea, not a specific implementation. This vault's CLAUDE.md fills in the specifics.

## See Also

- [[LLM-Maintained Wiki]] — the core concept this source defines
- [[Retrieval-Augmented Generation]] — contrasting approach
- [[Andrej Karpathy]] — author profile
- [[Memex]] — historical precedent
