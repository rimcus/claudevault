---
title: "Codex"
type: entity
entity_kind: tool
tags: [tool, coding-agent, openai]
created: 2026-08-07
updated: 2026-08-07
sources: [codyschneider-ai-citation-loop]
---

# Codex

*OpenAI's coding agent — the first non-Claude coding agent named in this wiki's Schneider corpus.*

## Background

Every prior Schneider pipeline in this wiki names Claude Code as the coding-agent layer. [[sources/codyschneider-ai-citation-loop]] is the first to name a different agent — "codex" — specifically for the fetch-and-analyze step (pulling the top 20 cited URLs and identifying their structural commonalities), while the subsequent write step is explicitly assigned to Claude Code ("hey claude code, build this"). [low confidence: the post's phrasing is casual enough ("have codex code fetch") that this could reflect a deliberate two-agent architecture or simply loose writing — captured as stated, not resolved]

## Role in This Wiki

The citation-research step in [[concepts/citation-shape-engineering|citation shape engineering]]: fetches the top-cited URLs for target prompts and extracts their structural commonalities, ahead of Claude Code's write step.

## Key Contributions / Actions

- Fetches and analyzes top-cited competitor URLs for structural patterns, per [[sources/codyschneider-ai-citation-loop]].

## See Also

- [[concepts/citation-shape-engineering]] — the pipeline this tool's step feeds
- [[sources/codyschneider-ai-citation-loop]] — source
