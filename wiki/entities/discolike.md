---
title: "Discolike"
type: entity
entity_kind: tool
tags: [tool, mcp, database, claude-code, cold-email]
created: 2026-04-15
updated: 2026-04-15
sources: [nickabraham-claude-code-campaign-lists]
---

# Discolike

An MCP (Model Context Protocol) provider that connects Claude Code to contact databases. Used by [[Nick Abraham]] to enable Claude to search, QA, and finalize cold email campaign lists directly from his database — without manual data exports or handoffs.

## Role in This Wiki

Represents the **MCP layer** in Claude Code GTM workflows — the connection between Claude's reasoning capabilities and underlying business data. Abraham's insight: MCP quality is the ceiling on what Claude Code can do. The LLM is capable; the bottleneck is the quality and breadth of the tools it can access.

## Position in Stack

```
Discolike MCP → Claude Code (search + QA + list finalization) → Airtable (campaign-ready output)
```

## See Also

- [[sources/nickabraham-claude-code-campaign-lists]] — primary source
- [[Nick Abraham]] — the practitioner who uses it
- [[Schema-Governed LLM Behavior]] — the trained context that makes the MCP connection intelligent
- [[sources/salescaptain-claude-code-gtm-playbook]] — the broader Claude Code GTM framework (Connections layer)
