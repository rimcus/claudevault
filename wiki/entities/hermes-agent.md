---
title: "Hermes Agent"
type: entity
entity_kind: tool
tags: [tool, ai-agent, runtime, gtm]
created: 2026-04-14
updated: 2026-08-11
sources: [codyschneider-gtm-agents, codyschneider-ai-media-company-playbook, codyschneider-two-agents-podcast]
---

# Hermes Agent

An AI agent framework recommended by [[Cody Schneider]] as the runtime for the [[AI Marketing Stack]]. Deployed on a [[Hetzner]] VPS to run always-on [[GTM Agents]].

## Role in This Wiki

The agent execution layer in Schneider's stack. Receives an [[OpenRouter]] API key and orchestrates the various GTM workflows.

## Key Contributions / Actions

- Runs the scraping/research step in [[concepts/directory-website-seo-play|the directory website tactic]] — builds the company dataset that Claude Code then designs a directory site around ([[sources/codyschneider-ai-media-company-playbook]]).

## Later Tension: "Agent Frameworks Are Usually Bloat" (August 2026)

[[sources/codyschneider-two-agents-podcast]], four months after this framework was first recommended, states that "agent frameworks are usually bloat for finite problems" — see [[concepts/agent-architecture-principles]]. Schneider doesn't reference Hermes Agent by name in the later post, and it's unclear whether the critique is meant to include it. Logged as an open tension rather than resolved either way.

## See Also

- [[AI Marketing Stack]] — the stack it anchors
- [[GTM Agents]] — the workflows it runs
- [[concepts/directory-website-seo-play]] — a specific workflow it executes
- [[concepts/agent-architecture-principles]] — later post questioning whether agent frameworks are worth the overhead
- [[Cody Schneider]] — recommended it
- [[sources/codyschneider-gtm-agents]] — source
- [[sources/codyschneider-ai-media-company-playbook]] — source
- [[sources/codyschneider-two-agents-podcast]] — the later, unreconciled critique
