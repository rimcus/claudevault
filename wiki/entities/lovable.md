---
title: "Lovable"
type: entity
entity_kind: tool
tags: [tool, ai-app-builder, saas, vibe-coding, frontend, supabase]
created: 2026-06-10
updated: 2026-06-10
sources: [theory-fb-ads-library-claude-saas]
---

# Lovable

An AI app builder that generates full-stack web applications from a single natural-language prompt. Accepts structured prompts describing backend logic (database tables, auth flows, APIs) and frontend layout, and produces a working app — typically 75–80% of a production MVP in one session.

## Role in This Wiki

The **rapid build layer** in the [[Ad Library Market Validation]] workflow. Given a Claude-generated prompt specifying [[Supabase]] backend logic and frontend layout, Lovable compresses the build phase from weeks to days.

## Key Properties

- Accepts highly structured prompts (auth, DB schema, API flows, UI layout)
- Output is a real codebase, not a prototype — can be connected to Supabase, Stripe, Vercel
- **Lovable Cloud vs. self-hosted Supabase:** Lovable offers its own hosted backend, but practitioners recommend switching to a real Supabase project before onboarding paying users — Lovable Cloud is "just a more expensive wrapper"
- 75–80% app completion in one session is the reported benchmark; remaining 20–25% requires manual fixes

## Position in Stack

```
Claude (generates Lovable-ready prompt) → Lovable (generates app) → Supabase + Stripe + Vercel (production)
```

## See Also

- [[Ad Library Market Validation]] — the workflow that uses Lovable as the build step
- [[sources/theory-fb-ads-library-claude-saas]] — primary source; £2,950 MRR across 6 tools built with this stack
- [[entities/higgsfield]] — MCP connector that enriches Claude's output before pasting into Lovable
