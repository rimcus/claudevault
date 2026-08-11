---
title: "Two GTM Agents: Signal-Based Cold Outbound + Organic LinkedIn Content Engine"
type: source
tags: [gtm-agents, linkedin, signal-infrastructure, enrichment, cold-email, content, agent-architecture]
created: 2026-08-11
updated: 2026-08-11
sources: [codyschneider-two-agents-podcast]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2086936003869393025"
source_type: x-post
---

# Two GTM Agents: Signal-Based Cold Outbound + Organic LinkedIn Content Engine

**Author:** [[entities/cody-schneider|Cody Schneider]] (@codyschneider)
**Published:** 2026-08-10/11
**Context:** A recap/timestamp post for [[entities/cody-schneider|Schneider]]'s appearance on [[entities/greg-isenberg|Greg Isenberg]]'s podcast. Rather than a single tactic, the post is a dense bullet-point map of two complete agent systems: an evolved, more automated version of the LinkedIn-engager cold-outbound pipeline first introduced in [[sources/codyschneider-gtm-agents]] (April 2026), and a new second system — an organic LinkedIn content agent — not previously covered in this wiki.

## Core Thesis

Two agents, two different jobs, one shared design philosophy: an agent is **code + a thinking loop + a live data stream**, built to model what a human already does manually — not an autonomous system reinvented from scratch. See [[concepts/agent-architecture-principles]].

**Agent one** (cold outbound): source leads from LinkedIn engagement (a hand-raise signal that beats firmographic targeting), run them through ICP-fit research before spending on enrichment, waterfall-enrich cheap-to-expensive, validate, and send from protected burner-domain infrastructure — with an inbox agent that manages replies and books demos, plus a six-month re-touch cycle for cold leads.

**Agent two** (organic content): stop prompting an LLM to "write good LinkedIn content" — it produces generic, AI-flaggable output. Instead mine content that already exists in internal conversations (interviews, sales calls, Slack, Notion, Gong), schedule it across accounts, and let a live analytics stream tell the agent what to snowball or remix.

## Key Points — Agent One: Signal-Based Cold Outbound

- LinkedIn engagement (reactions + comments) is a hand-raise signal that outperforms firmographic targeting.
- Track 10–20 category-outlier creators/accounts to get ~80% coverage of an entire industry — don't try to track every account in a category.
- Source creators from your own **For You feed**, not LinkedIn search — search surfaces stale, generic results.
- **Business accounts** (company pages), not just personal profiles, work as engagement sources too.
- [[entities/apify|Apify]] "Maestro" actors are named as the most stable LinkedIn scrapers currently available.
- The engager list is built from **post reactions plus post comments together** — either alone is an incomplete list.
- A **daily cron job** pulls net-new posts from tracked accounts, then extracts engagers from each — this is the automation cadence that keeps the source list current.
- **ICP-fit research happens before enrichment, not after** — a sequencing rule that avoids spending enrichment budget on people who wouldn't qualify anyway.
- Waterfall enrichment: cheapest accurate source first, most expensive last (see [[concepts/enrichment-waterfall]]).
- [[entities/origami|Origami]] aggregates the entire enrichment waterfall behind a single API call.
- [[entities/leadmagic|LeadMagic]] is called out specifically for **mobile phone number** enrichment.
- [[entities/millionverifier|MillionVerifier]] validates before sending — skip it and deliverability collapses fast.
- Buying broker contact data is legal; usage rules differ (a compliance nuance, not addressed further in the post).
- **Burner domains** protect the core business domain from deliverability damage.
- **Four domain buckets**: cold, marketing, transactional, business — a fuller taxonomy than "outreach domain vs. core domain."
- Roughly **$200/month** total infrastructure spend to start sending at 10k volume.
- [[entities/instantly|Instantly]] webhooks push positive replies to the inbox agent.
- The **inbox agent** answers prospect questions and drives the conversation toward a booked demo.
- A **six-month re-touch** program is scheduled to revive leads that went cold.
- **Calendar access is wired directly into the agent** so it can verify an actual booking happened — not just claim one did.

## Key Points — Agent Architecture Philosophy

- An agent equals: code + a thinking (LLM) loop + a live data stream — not a monolithic autonomous system.
- Don't pay LLM tokens for work cheap deterministic CPU logic can already do.
- Agent frameworks are usually bloat for problems that are actually finite and well-specified.
- Design the agent to model the human's real existing process — not an idealized "autonomous god-box" that reinvents the workflow.

See [[concepts/agent-architecture-principles]] for the full extraction and a flagged tension with Schneider's own earlier framework recommendation.

## Key Points — Agent Two: Organic LinkedIn Content Engine

- Organic content sourcing channels: interviews, sales calls, Slack, Notion, Gong — material that already exists rather than material an LLM invents.
- Prompting an LLM to "write good LinkedIn content" from a blank prompt produces mid, generic, AI-flaggable output.
- The thesis: the best content is already trapped in internal conversations, waiting to be extracted rather than generated.
- [[entities/ordinal|Ordinal]] schedules posts across multiple accounts and feeds analytics data back into the agent.
- The analytics stream tells the agent what to **snowball** (double down) or **remix** (repurpose into a new format).
- Repost proven winners every 90 days — explicitly **never** on a daily cadence.
- Apply the same "find what the market wants, then build" logic to content that Schneider applies to product validation elsewhere in the wiki (see [[concepts/ad-library-market-validation]]).
- LinkedIn paid impressions run roughly **$22 per thousand** — cited as the cost baseline that makes earned/organic media the better trade when it works.
- **Topic-based pages** (not tied to one person's identity) work as a substitute channel when a personal brand isn't appealing or available — see [[concepts/founder-brand-strategy]].

See [[concepts/organic-content-agent-loop]] for the full extraction.

## Timestamps (from source)

- 2:28 — Agent one: signal-based cold outbound
- 9:11 — Apify scraping and extracting engagers
- 15:47 — Waterfall enrichment, validation, compliance
- 21:40 — Inbox infrastructure, sending, inbox-managing agent
- 31:41 — Agent two: organic LinkedIn content engine

## Entities Mentioned

- [[entities/apify|Apify]] — LinkedIn scraping via Maestro actors
- [[entities/origami|Origami]] — enrichment waterfall aggregator (new)
- [[entities/leadmagic|LeadMagic]] — mobile phone enrichment specialization
- [[entities/millionverifier|MillionVerifier]] — pre-send validation (new entity page; previously only a dangling link)
- [[entities/instantly|Instantly]] — sending + webhook layer + inbox agent
- [[entities/ordinal|Ordinal]] — cross-account LinkedIn scheduler + analytics feedback (new)
- [[entities/greg-isenberg|Greg Isenberg]] — podcast host (new)

## Concepts Touched

- [[concepts/agent-architecture-principles]] — new concept; the cross-cutting design philosophy
- [[concepts/organic-content-agent-loop]] — new concept; the content-mining + scheduling + feedback system
- [[concepts/signal-infrastructure]] — extended with LinkedIn sourcing mechanics (for-you feed, category outliers, engager extraction)
- [[concepts/enrichment-waterfall]] — extended with Origami, MillionVerifier, ICP-fit-before-enrichment ordering, broker-data compliance note
- [[concepts/cold-email-infrastructure]] — extended with the four-domain-bucket taxonomy and the ~$200/month cost anchor
- [[concepts/hybrid-ai-model]] — the "don't pay tokens for what cheap CPU does" principle is a compute-layer restatement of the same automate/reserve-judgment split
- [[concepts/founder-perspective-content-moat]] — sibling claim: valuable content already exists in unstructured internal material, waiting to be extracted rather than generated
- [[concepts/content-outbound-flywheel]] — a different mechanism for the same content+outbound-on-LinkedIn territory
- [[concepts/founder-brand-strategy]] — topic-based pages as the alternative when personal brand doesn't fit

## My Notes

This post is Schneider's most explicit statement yet of an agent-building philosophy, and it sits in real tension with his own April post ([[sources/codyschneider-gtm-agents]]), which recommended [[entities/hermes-agent|Hermes Agent]] as the runtime framework for GTM agents. Four months later he states "agent frameworks are usually bloat for finite problems." Both posts are his own; neither references the other. Logged as an open tension in [[concepts/agent-architecture-principles]] rather than silently reconciled.

The cold-outbound agent described here is a clear evolution of the April pipeline (Apify → Apollo → Million Verifier → Instantly) — same shape, more automation (daily cron, ICP-fit-first ordering) and different named tools (Origami as an aggregator, LeadMagic named specifically for mobile numbers).

## See Also

- [[sources/codyschneider-gtm-agents]] — the earlier, less automated version of the same cold-outbound pipeline
- [[concepts/agent-architecture-principles]] — extracted design philosophy
- [[concepts/organic-content-agent-loop]] — extracted content system
- [[concepts/signal-infrastructure]] — updated with this post's sourcing mechanics
- [[concepts/enrichment-waterfall]] — updated with this post's providers and ordering rule
- [[concepts/cold-email-infrastructure]] — updated with the domain-bucket taxonomy
- [[entities/cody-schneider]] — author
