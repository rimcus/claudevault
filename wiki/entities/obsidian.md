---
title: "Obsidian"
type: entity
entity_kind: tool
tags: [tool, markdown, knowledge-management, note-taking]
created: 2026-04-14
updated: 2026-04-14
sources: [karpathy-llm-wiki-pattern]
---

# Obsidian

A local-first markdown note-taking application with a graph view, wikilink syntax, and a rich plugin ecosystem. Used as the browsing interface ("the IDE") in the [[LLM-Maintained Wiki]] pattern.

## Role in This Wiki

This vault *is* an Obsidian vault. Obsidian provides the interface for browsing, navigating, and visualizing the wiki while the LLM writes and maintains it.

## Key Features Relevant to the LLM Wiki Pattern

- **Wikilink syntax** (`[[Page Title]]`) — the basis for inter-page linking and graph construction
- **Graph view** — visualizes which pages are hubs, which are orphans, how concepts cluster
- **Dataview plugin** — runs queries over YAML frontmatter; enables dynamic tables and lists
- **Marp plugin** — renders markdown as slide decks
- **Web Clipper** — browser extension that converts web articles to markdown for ingestion
- **Attachment download** — hotkey to download all images in a note to local disk (`raw/assets/`)

## Obsidian Setup for LLM Wiki

In Obsidian Settings:
- **Files and links → Attachment folder path:** `raw/assets/` (keeps images organized)
- **Hotkeys → "Download attachments for current file":** bind to e.g. Ctrl+Shift+D

Recommended plugins:
- Dataview
- Marp (for slide decks)
- Templater (for templates)
- Git (for version history)

## See Also

- [[LLM-Maintained Wiki]] — the pattern Obsidian serves as the IDE for
- [[Andrej Karpathy]] — recommended Obsidian for this use case
- [[Dataview]] — plugin for querying frontmatter
- [[Marp]] — plugin for slide decks
