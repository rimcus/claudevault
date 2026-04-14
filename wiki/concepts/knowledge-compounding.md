---
title: "Knowledge Compounding"
type: concept
tags: [knowledge-management, llm, wiki, value-proposition]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern]
---

# Knowledge Compounding

The property of a knowledge system whereby each addition makes all previous additions more valuable, because new information is integrated with — rather than stored alongside — existing knowledge. Contrast with linear accumulation, where each new document is simply appended to a pile.

## Overview

In a compounding knowledge system, adding source N doesn't just give you N sources to search — it potentially updates the synthesis on every existing page that source touches. Cross-references from existing pages to new concepts are added. Contradictions with existing claims are flagged. The overview is revised to reflect the fuller picture.

This is the central value proposition of the [[LLM-Maintained Wiki]] pattern, and the property that [[Retrieval-Augmented Generation]] lacks. RAG accumulates documents linearly; the LLM wiki compounds them.

## Key Properties / Characteristics

- **Integration > accumulation:** New information is woven into existing structure, not appended.
- **Cross-references as value:** The connections between pages are as valuable as the pages themselves (cf. [[Memex]]).
- **Synthesis preservation:** The current best understanding is always written down — you don't have to re-derive it.
- **Contradiction tracking:** The system knows when sources disagree; the human doesn't have to hold this in their head.

## Why Humans Fail at This

Human-maintained wikis (Confluence, Notion, personal wikis) fail to compound because maintenance is tedious:
- Updating cross-references when a new source arrives is unglamorous work
- It's easy to forget which pages a new source is relevant to
- Consistency across dozens of pages requires re-reading all of them

LLMs don't have these failure modes: they don't get bored, have near-total recall of all pages they've read, and can touch 15 files in a single pass.

## See Also

- [[LLM-Maintained Wiki]] — the system designed to achieve knowledge compounding
- [[Retrieval-Augmented Generation]] — the approach that lacks this property
- [[Memex]] — Bush's vision of associative trails as the mechanism for compounding
