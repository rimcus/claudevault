---
title: "Agent Specialization by Context Window"
type: concept
tags: [ai-coding, agent-orchestration, context-engineering, code-quality, claude-code]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# Agent Specialization by Context Window

*Named, stable, domain-specialized coding agents — each launched with a deliberately bounded, guaranteed context — orchestrated by an intent-reading dispatcher agent, as the fix for a specific AI-coding quality plateau: features that are "integrated" into a codebase without being "assimilated" into it.*

## Overview

The most novel material from [[entities/maxime-champoux|Maxime Champoux]]'s account of building [[entities/well|Well]]. The team plateaued at 40–50 shipped features/month for two months (March–April) despite the marginal-gains tooling discipline described in [[concepts/marginal-gains-1-percent]]. They deliberately slowed shipping to instrument and root-cause the plateau using OpenTelemetry (OTel) to capture every terminal interaction across the team's Claude Code and Codex sessions — prompts, retrieved context documents, agents invoked — specifically to diagnose recurring quality regressions.

## Key Properties / Characteristics

- Diagnosis: a feature can be "integrated" (works in isolation, passes its own automated tests) without being "assimilated" (doesn't account for the rest of the system, silently breaks existing behavior).
- Root cause of failed assimilation: **"code patina"** — the accumulated, often non-obvious historical reasons behind specific detours in how code is actually written, invisible from reading the code alone.
- Fix requires two things together, not either alone: (1) documenting the reasoning behind a patina detour, and (2) an agent specialized enough in that part of the codebase that its context window isn't overwhelmed trying to hold the whole system in mind.
- 8 named, stable specialized agents, each mapped to a specific production-cycle role (e.g., design, data-model, connectors, design-system/table-generation).
- Each specialized agent launches with a guaranteed baseline context (its own domain documentation), expandable with adjacent documentation as a given task requires.
- An orchestrator agent reads a feature's intent and deploys the correct specialized agent(s) for the job.
- Explicit rule: never let a generic, unspecialized agent execute specialized work — purely a quality decision, not a capability limitation (a generic agent could technically attempt it, the way a human could technically attempt work outside their specialty, but reliably produces worse output).

## How It Works

**Diagnosing the plateau.** OTel-captured session data let the team trace specific production quality regressions back to their originating prompts/agents/context, rather than guessing. The pattern that emerged: regressions clustered around cases where an agent, lacking awareness of why a piece of code was written a specific (non-obvious) way, took the more direct-looking implementation path instead — silently reintroducing a previously-fixed bug or breaking an adjacent behavior.

**Building the fix.** Bottom-up, before it became official policy: individual engineers began "personifying" quality-review agents — one example given is an engineer building a "Claude as Maxime" persona to review every PR the way Champoux himself would. Every time that review surfaces a quality gap (example given: a missing translation), the response isn't just to patch that instance — it's to create a new reusable **skill** so the entire defect class can't recur, fed into the team's shared pipeline so every engineer benefits, not just the one who found it. This bottom-up pattern generalized into the 8 named specialized agents plus orchestrator described above. In April, documentation was also moved from an external tool (Notion) directly into the codebase, so both humans and agents draw from the same, co-located source of truth.

**The generalizable heuristic — when do you need to specialize at all?** Champoux frames it as a context-window/cognitive-load capacity question: if a generic agent can hold your entire relevant documentation and/or codebase inside its context window, you don't need specialized agents (or need only light steering). Once the material required to do a task well exceeds what a single context window can responsibly hold without degrading output quality, that's the trigger to split into named, bounded, specialized agents. He offers documentation size / lines of code as a rough proxy for this threshold — directly drawing the parallel to his own experience scaling Qonto's *human* product org from 2 people (no need to specialize) to 150 (forced into specialized squads as the product surface grew past what any one person could hold in their head) — see [[concepts/toyota-production-system-for-software]].

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/maximechampoux-well-ai-native-engineering]] | Well runs 8 named, stable specialized agents orchestrated by an intent-reading dispatcher | high (specific, first-person architectural claim) |
| [[sources/maximechampoux-well-ai-native-engineering]] | This fix took the team from a 40–50/month plateau to 100+/month | high (dated, specific before/after claim from the founder) |
| [[sources/maximechampoux-well-ai-native-engineering]] | Context-window capacity relative to documentation/codebase size is the correct trigger for when to specialize agents | medium (a stated heuristic/opinion, not validated against a benchmark or threshold number) |

## Contradictions & Open Questions

- No specifics given on exactly what "guaranteed baseline context" means in practice for each of the 8 agents (token budget, specific document set) — described at the policy level, not the implementation level.
- Open question: how does the orchestrator itself avoid the same integration-vs-assimilation failure mode when a feature genuinely spans multiple specialized domains at once (e.g., a feature touching both the data model and the connector layer) — does it deploy agents sequentially, in parallel, or does one specialized agent hand off to another?
- This concept is structurally the engineering-side analog of this wiki's existing [[concepts/gtm-agents]] "agents write their own skill files" pattern and [[concepts/schema-governed-llm-behavior]] — worth treating as convergent evidence that the same "bounded, named, self-documenting agent" pattern generalizes across both GTM and core engineering, from two unrelated sources.

## See Also

- [[concepts/toyota-production-system-for-software]] — the human-team specialization precedent this heuristic is drawn from
- [[concepts/ai-native-engineering-team]] — the velocity context this fix operated inside
- [[concepts/schema-governed-llm-behavior]] — the wiki's existing CLAUDE.md-as-persistent-memory concept, the closest analog to Well's in-codebase skills documentation
- [[concepts/gtm-agents]] — the GTM-side parallel: agents that write their own skill files
- [[sources/maximechampoux-well-ai-native-engineering]] — primary source
