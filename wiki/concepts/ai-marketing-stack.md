---
title: "AI Marketing Stack"
type: concept
tags: [ai-agents, gtm, tools, infrastructure, marketing]
created: 2026-04-14
updated: 2026-04-14
sources: [codyschneider-gtm-agents]
---

# AI Marketing Stack

The minimum set of infrastructure required to run autonomous [[GTM Agents]]: an always-on agent runtime, an LLM API gateway, and a data warehouse. Popularized by [[Cody Schneider]]'s 2026 thread as a setup deployable in under 10 minutes.

## The Stack

### Tier 1: Core Infrastructure
| Layer         | Tool                                | Notes                                                       |
| ------------- | ----------------------------------- | ----------------------------------------------------------- |
| Agent runtime | [[Hermes Agent]] on [[Hetzner]] VPS | Hetzner chosen for cost; always-on execution                |
| LLM access    | [[OpenRouter]] → MiniMax 2.7        | OpenRouter as gateway; MiniMax 2.7 as the workhorse model   |
| Data backbone | Open-source data warehouse          | All business data flows here; agents query it for decisions |

### Tier 2: Lead Generation Tools
| Tool | Function |
|------|----------|
| [[Apify]] | Web scraping (LinkedIn, etc.) |
| [[Apollo]] | B2B contact enrichment, email finding |
| [[entities/millionverifier|MillionVerifier]] | Email verification before sending |
| [[Instantly]] | Cold email sending + inbox management |

### Tier 3: SEO & Content Tools
| Tool | Function |
|------|----------|
| [[Ahrefs]] | Keyword research, competitor analysis (MCP integration) |
| CMS API | Publishing landing pages and blog posts |
| [[PostHog]] | Product analytics, tracking content-driven signups |

### Tier 4: CRM & Email
| Tool | Function |
|------|----------|
| [[HubSpot]] | CRM; enriched by agent hourly |
| [[Exa API]] | Web research for contact enrichment |
| [[SendGrid]] | Transactional + marketing email delivery |

## Why the Data Warehouse is the Critical Layer

Without a data warehouse, agents operate on snapshots and guesses. With it:
- Ad agents can optimize against real conversion data
- SEO agents can rank content initiatives by projected revenue impact
- Email agents can A/B test against activation metrics
- All agents share a common ground truth

## Key Properties

- **Composable:** each tier can be swapped out independently
- **MCP-native:** Ahrefs, and potentially other tools, integrate via MCP rather than custom API code
- **Low fixed cost:** Hetzner VPS is cheap; OpenRouter is pay-per-token

## See Also

- [[GTM Agents]] — what this stack runs
- [[Data Warehouse for AI]] — the critical enabling component
- [[Cody Schneider]] — defined this stack
- [[sources/codyschneider-gtm-agents]] — source
