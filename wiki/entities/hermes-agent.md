---
title: "Hermes Agent"
type: entity
entity_kind: tool
tags: [tool, ai-agent, runtime, gtm]
created: 2026-04-14
updated: 2026-07-17
sources: [codyschneider-gtm-agents, codyschneider-ai-media-company-playbook]
---

# Hermes Agent

An AI agent framework recommended by [[Cody Schneider]] as the runtime for the [[AI Marketing Stack]]. Deployed on a [[Hetzner]] VPS to run always-on [[GTM Agents]].

## Role in This Wiki

The agent execution layer in Schneider's stack. Receives an [[OpenRouter]] API key and orchestrates the various GTM workflows.

## Key Contributions / Actions

- Runs the scraping/research step in [[concepts/directory-website-seo-play|the directory website tactic]] — builds the company dataset that Claude Code then designs a directory site around ([[sources/codyschneider-ai-media-company-playbook]]).

## See Also

- [[AI Marketing Stack]] — the stack it anchors
- [[GTM Agents]] — the workflows it runs
- [[concepts/directory-website-seo-play]] — a specific workflow it executes
- [[Cody Schneider]] — recommended it
- [[sources/codyschneider-gtm-agents]] — source
- [[sources/codyschneider-ai-media-company-playbook]] — source
