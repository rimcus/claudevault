---
title: "LLM-Maintained Wiki"
type: concept
tags: [llm, knowledge-management, wiki, methodology, core-concept]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern]
---

# LLM-Maintained Wiki

A pattern for building personal knowledge bases in which an LLM incrementally writes and maintains a structured, interlinked wiki of markdown files — rather than merely retrieving from raw documents at query time. The wiki is a persistent, compounding artifact that grows richer with every source added and every question asked.

## Overview

The core distinction from [[Retrieval-Augmented Generation]] is that knowledge is *compiled* once and *kept current*, not re-derived on every query. When a new source is added, the LLM doesn't just index it — it reads it, extracts key information, integrates it into existing pages, flags contradictions, and strengthens the synthesis. Cross-references are already built; the LLM doesn't have to rediscover them each time.

The pattern was articulated by [[Andrej Karpathy]] in a 2026 gist. This vault is an instantiation of it.

## Three Layers

| Layer | Contents | Who writes it |
|-------|----------|---------------|
| Raw sources | Immutable source documents (articles, papers, etc.) | Human (curates) |
| Wiki | Markdown pages: summaries, concepts, entities, analyses | LLM (writes & maintains) |
| Schema | CLAUDE.md / AGENTS.md governing LLM behavior | Human + LLM (co-evolve) |

## Key Properties / Characteristics

- **Compounding:** Each source adds to a permanent structure rather than disappearing into chat history.
- **Cross-referenced by default:** Entity and concept pages are updated on every ingest. Links exist before you think to ask for them.
- **Contradiction-aware:** The LLM flags when new sources conflict with existing claims rather than silently overwriting.
- **Maintenance-free for humans:** LLMs don't get bored, don't forget to update cross-references, and can touch 15 files in one pass.
- **Schema-governed:** The LLM's behavior is defined in a schema document, making it disciplined rather than ad-hoc.

## Operations

- **Ingest** — add a source → LLM touches 5–15 pages, updates index and log
- **Query** — ask a question → LLM reads relevant pages, synthesizes, optionally files answer back as an analysis page
- **Lint** — periodic health check → find orphans, contradictions, missing pages, stale claims

## How It Works (Workflow)

1. Human drops source into `raw/sources/`
2. LLM reads source, discusses takeaways with human
3. LLM writes `wiki/sources/<slug>.md`
4. LLM updates all relevant concept and entity pages
5. LLM updates `wiki/index.md` and appends to `wiki/log.md`
6. Human browses results in [[Obsidian]], gives feedback

## Variants / Subtypes

- **Personal** — goals, health, psychology, journal entries
- **Research** — papers, articles, evolving thesis
- **Book companion** — per-chapter filing, character/theme pages
- **Team/business** — fed by Slack, meeting transcripts, customer calls
- **Topic deep-dives** — competitive analysis, due diligence, travel planning

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/karpathy-llm-wiki-pattern]] | LLMs touching 5–15 pages per ingest is typical | medium |
| [[sources/karpathy-llm-wiki-pattern]] | Index file is sufficient navigation up to ~100 sources | medium |

## Contradictions & Open Questions

- Open question: At what wiki scale does the index approach break down and require proper search (like [[qmd]])?
- Open question: How should this pattern adapt for multi-user / team settings where multiple humans are curating?

## See Also

- [[Retrieval-Augmented Generation]] — the contrasting approach
- [[Memex]] — 1945 predecessor concept
- [[Andrej Karpathy]] — originator of this pattern
- [[Schema-Governed LLM Behavior]] — the mechanism that makes the LLM disciplined
- [[Knowledge Compounding]] — the key value proposition
