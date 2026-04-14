---
title: "qmd"
type: entity
entity_kind: tool
tags: [tool, search, markdown, cli, mcp]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern]
---

# qmd

A local search engine for markdown files with hybrid BM25/vector search and LLM re-ranking, all on-device. Recommended by [[Andrej Karpathy]] as a CLI tool for searching the wiki as it grows beyond what the index file alone can handle.

## Role in This Wiki

Optional future tool. At small scale, `wiki/index.md` is sufficient for navigation. As the wiki grows to hundreds of pages, qmd provides proper search without needing external embedding infrastructure.

## Interfaces

- **CLI** — the LLM can shell out to it for search queries
- **MCP server** — the LLM can use it as a native tool (no shell required)

## When to Add It

When `wiki/index.md` becomes unwieldy (rough threshold: 100+ sources, 200+ pages) or when search over full page content becomes necessary rather than just the index.

## See Also

- [[LLM-Maintained Wiki]] — the context in which this tool is recommended
- [[Andrej Karpathy]] — recommended this tool
