---
title: "Schema-Governed LLM Behavior"
type: concept
tags: [llm, prompt-engineering, workflow, methodology]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern]
---

# Schema-Governed LLM Behavior

The practice of defining an LLM's operational conventions in a persistent configuration document (e.g. `CLAUDE.md`, `AGENTS.md`) that the LLM reads at the start of each session. This makes the LLM a disciplined, consistent operator of a system — rather than a generic chatbot that behaves differently each session.

## Overview

Without a schema, an LLM operating on a wiki would invent its own conventions each session: different page formats, inconsistent linking, forgotten workflows. With a schema, the LLM is told exactly how the wiki is structured, what files to create, what frontmatter to use, and what steps to follow for each operation type.

In the [[LLM-Maintained Wiki]] pattern, the schema document is the key configuration file. The human and LLM co-evolve it over time as they discover what conventions work for their domain.

## Key Properties / Characteristics

- **Persistent across sessions** — the schema is a file, not a prompt; it survives conversation resets
- **Co-evolved** — the human and LLM refine it together as the system matures
- **Operations-oriented** — defines workflows (ingest, query, lint) not just page formats
- **Domain-adaptable** — the same pattern applies to wildly different knowledge domains; only the schema changes

## How It Works

1. At session start, LLM reads the schema document
2. Schema defines: directory layout, page frontmatter, naming conventions, linking conventions, workflow steps for each operation type
3. LLM follows these conventions throughout the session
4. When the human identifies improvements, the schema is updated and governs future sessions

## Variants

- **CLAUDE.md** — the convention for Claude Code (Anthropic)
- **AGENTS.md** — the convention for OpenAI Codex
- Domain-specific extensions: adding domain conventions (e.g. citation formats for academic wikis, field definitions for business wikis)

## See Also

- [[LLM-Maintained Wiki]] — the system this concept governs
- [[Andrej Karpathy]] — described this as the "key configuration file" of the pattern
