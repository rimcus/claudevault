---
title: "Nick Abraham"
type: entity
entity_kind: person
tags: [person, cold-email, linkedin, outbound, claude-code, mcp, inmail]
created: 2026-04-15
updated: 2026-07-09
sources: [nickabraham-claude-code-campaign-lists, nickabraham-linkedin-inmail-pipeline]
---

# Nick Abraham

Outbound practitioner at significant scale: 15+ concurrent campaigns, 250,000+ LinkedIn InMails/month. Active on X (@NickAbraham12). Documents what works operationally — not theory, current live systems.

## Role in This Wiki

Represents the **operational practitioner** perspective on GTM at scale — distinct from Stathopoulos (agency playbook), Vacca (empirical/role definition), and Schneider (builder/tools). Abraham ships live systems and documents failure modes discovered in production.

## Key Claims

| Claim | Source |
|-------|--------|
| 15+ concurrent cold email campaigns managed via Claude Code + MCP | [[sources/nickabraham-claude-code-campaign-lists]] |
| Cut campaign list management from 5 hours to 2 hours (with better output) | [[sources/nickabraham-claude-code-campaign-lists]] |
| Claude handles org hierarchy — finds correct title when ICP title doesn't exist at smaller companies | [[sources/nickabraham-claude-code-campaign-lists]] |
| "Building your own MCPs/endpoints is 100% where your time should be spent right now" | [[sources/nickabraham-claude-code-campaign-lists]] |
| 250,000+ LinkedIn InMails/month across 15+ campaigns | [[sources/nickabraham-linkedin-inmail-pipeline]] |
| 5-step list pipeline (GetLeads → NetNut → Apify → AI agent → sequencer) protects paid credit balance | [[sources/nickabraham-linkedin-inmail-pipeline]] |
| Sales Nav pulls run 30–40% open profiles vs. 5–8% for standard database pulls | [[sources/nickabraham-linkedin-inmail-pipeline]] |
| Sequencer must verify open-profile status at send time, not just at list-load | [[sources/nickabraham-linkedin-inmail-pipeline]] |

## See Also

- [[sources/nickabraham-claude-code-campaign-lists]] — Claude Code + Discolike MCP for campaign list management
- [[sources/nickabraham-linkedin-inmail-pipeline]] — LinkedIn InMail list pipeline at 250K+/month
- [[concepts/linkedin-inmail-pipeline|LinkedIn InMail Pipeline]] — synthesized concept page for the InMail system
- [[entities/discolike|Discolike]] — the MCP he uses to connect Claude to his contact database
- [[entities/getleads|GetLeads]] — list building tool in his InMail pipeline
- [[entities/netnut|NetNut]] — open-profile enrichment tool in his InMail pipeline
- [[GTM Engineering]] — his workflow is a live implementation of this concept
