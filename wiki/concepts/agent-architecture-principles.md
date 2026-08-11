---
title: "Agent Architecture Principles"
type: concept
tags: [ai-agents, architecture, gtm-engineering, tokens, cost, design-philosophy]
created: 2026-08-11
updated: 2026-08-11
sources: [codyschneider-two-agents-podcast]
---

# Agent Architecture Principles

*An agent is code plus a thinking loop plus a live data stream, built to model a human's real existing process — not an autonomous system reinvented from scratch, and not a general-purpose framework applied to a finite problem.*

## Overview

[[entities/cody-schneider|Cody Schneider]] states, across [[sources/codyschneider-two-agents-podcast]], a compact set of design rules for building narrow, working GTM agents rather than the more elaborate autonomous systems the term "AI agent" usually implies. The rules are opinionated and somewhat contrarian relative to the wiki's own earlier framework recommendation from the same author (see Contradictions below).

The core claim: most business problems agents get built for are *finite* — a bounded, describable process a human already runs. The job of the agent isn't to invent a smarter version of that process from first principles; it's to encode the process faithfully, use an LLM only for the steps that genuinely require judgment or generation, and use ordinary deterministic code for everything else.

## Key Properties / Characteristics

- **Agent = code + thinking loop + live data stream.** The LLM call is one component in a larger deterministic system, not the system itself.
- **Don't pay tokens for what cheap CPU already does.** Filtering, deduping, formatting, routing, and other deterministic logic belongs in plain code — not in an LLM prompt. This is a cost and reliability argument: code is cheaper and more consistent than an LLM call for anything that doesn't require judgment.
- **Agent frameworks are usually bloat for finite problems.** General-purpose orchestration frameworks add abstraction and failure surface that a well-scoped, hard-coded pipeline doesn't need, when the underlying business process is already bounded and known.
- **Model the human's real process, not an autonomous god-box.** Start from what a human currently does step by step — the actual workflow, including its shortcuts and judgment calls — rather than designing an idealized fully-autonomous system and hoping the LLM fills every gap.

## How It Works

In practice, applied to the cold-outbound agent in the same post: the LLM does ICP-fit judgment calls and inbox-agent conversation; plain code and API calls handle scraping, enrichment routing, validation, cron scheduling, and webhook handling. The "thinking loop" is invoked only where a human would actually stop and think — everywhere else, the pipeline runs deterministically.

## Relation to the Hybrid AI Model

[[concepts/hybrid-ai-model]] states the same underlying principle one layer up: AI on volume/judgment-light work, humans on judgment-heavy decisions, validated across three independent sources ([[entities/alex-vacca|Alex Vacca]]/[[entities/coldiq|ColdIQ]], [[entities/bill-stathopoulos|Bill Stathopoulos]]/[[entities/salescaptain|SalesCaptain]], [[entities/armand-farrokh|Armand Farrokh]]). This concept is the *implementation-layer* version of the same split, moved from the human/AI boundary down to the code/LLM boundary inside a single agent: reserve tokens for genuine judgment or generation, and let deterministic code carry everything else. Where the Hybrid AI Model asks "should a human or an AI do this step," Agent Architecture Principles asks "should a token-costing LLM call or a free CPU instruction do this step" — the same discipline, one level lower in the stack.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/codyschneider-two-agents-podcast]] | Agent = code + thinking loop + live data stream; frameworks are bloat for finite problems; model the human's process | low (asserted principles, no before/after data, no named framework being criticized) |

## Contradictions & Open Questions

- **Unreconciled with Schneider's own earlier post:** [[sources/codyschneider-gtm-agents]] (April 2026) recommends [[entities/hermes-agent|Hermes Agent]] as the runtime framework for GTM agents — a named agent framework. Four months later, this post states "agent frameworks are usually bloat for finite problems," with no reference back to the earlier recommendation. It's unclear whether Schneider now considers Hermes Agent itself bloat, is drawing a distinction between a lightweight runtime (Hermes) and a heavier orchestration framework (unnamed), or has simply changed his position. Treat as an open tension between two of his own posts rather than a settled stance — logged the same way the wiki already logs the [[concepts/founder-perspective-content-moat]] / [[concepts/citation-shape-engineering]] tension from the same author.
- No specific "bloated" framework is named, so the claim can't be checked against a concrete alternative.
- Open question: does "model the human's real process" scale to processes with no single human doing them today (i.e., genuinely new workflows), or is it specifically a retrofit heuristic for automating existing manual work?

## See Also

- [[sources/codyschneider-two-agents-podcast]] — primary source
- [[concepts/hybrid-ai-model]] — the human/AI-layer version of the same underlying split
- [[entities/hermes-agent|Hermes Agent]] — the framework this post's claim sits in tension with
- [[entities/cody-schneider|Cody Schneider]] — author of both the original framework recommendation and this later critique
- [[concepts/gtm-agents|GTM Agents]] — the broader practice this principle governs
