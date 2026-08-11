---
title: "Instantly"
type: entity
entity_kind: tool
tags: [tool, cold-email, outreach, sales]
created: 2026-04-14
updated: 2026-08-11
sources: [codyschneider-gtm-agents, codyschneider-two-agents-podcast]
---

# Instantly

A cold email platform for outreach campaigns. Used in [[Cody Schneider]]'s GTM stack as the sending layer and inbox management tool. The agent adds verified leads to Instantly campaigns and manages responses in the inbox.

## Pipeline Position

[[Apify]] → [[Apollo]] / [[entities/origami|Origami]] → [[entities/millionverifier|MillionVerifier]] → **Instantly** (send + manage inbox)

## Webhooks and the Inbox Agent (Schneider, August 2026)

[[sources/codyschneider-two-agents-podcast]] specifies the inbox side in more detail: Instantly webhooks push positive replies directly to an inbox-managing agent, which answers prospect questions and drives the conversation toward a booked demo. Two further details from the same post:

- **Six-month re-touch program** — leads that go cold are re-engaged on a scheduled six-month cadence rather than abandoned.
- **Calendar access wired into the agent** — the inbox agent has direct calendar access so it can verify an actual booking occurred, rather than just reporting that it asked for one.

## See Also

- [[GTM Agents]] — workflow context
- [[AI Marketing Stack]] — broader stack
- [[entities/millionverifier|MillionVerifier]] — feeds into Instantly
- [[sources/codyschneider-two-agents-podcast]] — inbox agent, webhooks, re-touch cadence, calendar verification
- [[concepts/agent-architecture-principles]] — the design philosophy behind the inbox agent
