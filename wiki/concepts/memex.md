---
title: "Memex"
type: concept
tags: [history-of-computing, knowledge-management, hypertext, vannevar-bush]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern]
---

# Memex

A hypothetical personal knowledge machine proposed by [[Vannevar Bush]] in "As We May Think" (The Atlantic, 1945). The Memex was envisioned as a desk-sized device storing all of a person's books, records, and communications — queryable via *associative trails* that linked related documents together, mimicking how human memory works by association rather than by index.

## Overview

Bush's key insight was that the value of a personal knowledge store lies not just in the documents themselves, but in the **trails between them** — the connections that reflect how you think about a topic. The Memex would let you annotate documents, create trails linking related materials, and share those trails with others.

The vision was private, actively curated, and associative — closer to the [[LLM-Maintained Wiki]] pattern than to the open, link-based web that actually emerged.

## Key Properties / Characteristics

- **Private and personal** — each person's Memex reflects their own reading and thinking
- **Associative trails** — connections between documents are as valuable as the documents themselves
- **Active curation** — the user is responsible for building and maintaining trails
- **The unsolved problem** — Bush had no solution to *who does the maintenance* as the collection grows

## How the LLM Solves Bush's Problem

The LLM-Maintained Wiki is essentially a Memex where the LLM handles maintenance:
- The human curates sources (as Bush imagined)
- The LLM builds and maintains the associative trails (what Bush couldn't automate)
- The wiki grows without the maintenance burden that causes human-maintained systems to collapse

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/karpathy-llm-wiki-pattern]] | Bush's Memex vision was closer to LLM wiki than to the web | medium |

## See Also

- [[Vannevar Bush]] — creator of the Memex concept
- [[LLM-Maintained Wiki]] — the modern realization
- [[Knowledge Compounding]] — the property the Memex was designed to achieve
