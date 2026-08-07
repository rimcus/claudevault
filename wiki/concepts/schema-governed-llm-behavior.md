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

## Convergent Evidence: The Same Pattern in Production Engineering

[[sources/maximechampoux-well-ai-native-engineering]] documents an independent, unrelated instance of this same pattern applied one layer down — not to a wiki or GTM workflow, but to a company's own production codebase. [[entities/well|Well]] moved its documentation from an external tool (Notion) directly into the codebase, and engineers turned recurring PR-review findings into reusable "skills" that get folded into a shared pipeline the moment they're discovered (see [[concepts/agent-specialization-context-window]]) — functionally the same "persistent, co-evolved, operations-oriented configuration" this concept describes, just version-controlled alongside the code it governs rather than living in a CLAUDE.md file. Worth treating as convergent evidence that this pattern generalizes beyond LLM wikis and GTM agents to AI-assisted software engineering itself.

## See Also

- [[LLM-Maintained Wiki]] — the system this concept governs
- [[Andrej Karpathy]] — described this as the "key configuration file" of the pattern
- [[concepts/agent-specialization-context-window]] — the same pattern applied to a production codebase instead of a wiki
- [[concepts/gtm-agents]] — the GTM-side instance: agents that write their own skill files
