---
title: "Cold Email Infrastructure"
type: concept
tags: [cold-email, outbound, deliverability, domains, inboxes, scaling, infrastructure]
created: 2026-04-15
updated: 2026-04-15
sources: [anon-cold-email-systems-guide]
---

# Cold Email Infrastructure

The technical architecture — domains, inboxes, warm-up, and sending limits — that determines whether cold emails land in the primary inbox or get flagged as spam. Deliverability is not a copywriting problem; it is an infrastructure problem. Getting the infrastructure wrong makes all other optimization irrelevant.

## The Three Components

### 1. Domains

Never send cold email from your primary business domain (e.g., `apple.com`). A single deliverability failure can blacklist your main domain, crashing the entire company's email communication.

Instead: buy **outreach-specific domains** (e.g., `useapple.com`, `tryapple.com`). These are sacrificial infrastructure — if a domain gets flagged, you retire it and spin up a new one without affecting the main business.

### 2. Inboxes

Individual email accounts set up on outreach domains (e.g., `steve@useapple.com`). Multiple inboxes per domain are standard. Each inbox is an independent sending unit.

### 3. Warm-Up

A **mandatory 14-day period** of automated, low-volume sending before any real campaign traffic. Purpose: prove to Google and Outlook that the account belongs to a human, not a bot. Skipping warm-up is the most common cause of new accounts going directly to spam.

## The Speed Limit: 20 Emails Per Day Per Inbox

The single most important rule in cold email infrastructure.

**Hard limit:** 20 emails/day/inbox. Exceeding this triggers spam filters ("Spam Jail") — and recovery is difficult to impossible for that inbox.

**How to scale:** Never increase the per-inbox rate. Instead, add more domains and inboxes. The relationship is linear:

| Inboxes | Daily Volume |
|---------|-------------|
| 1 | 20 |
| 5 | 100 |
| 25 | 500 |
| 50 | 1,000 |
| 100 | 2,000 |

This linear model makes the financial architecture predictable: volume scales with infrastructure spend, not with risk. It also means the economics of running cold email as a service are fundamentally about managing domain/inbox costs vs. per-call revenue.

## Deliverability Rules (Copy Layer)

Infrastructure alone is not sufficient. The copy must also be deliverability-safe:

- **Plain text only** — no HTML, no images, no links in the email body
- **No headshots in signatures**
- **No attachments**
- **Spin Tax Rule:** Vary copy at the sentence level using bracket notation `{variant A|variant B|variant C}` to prevent identical emails flagging your domain across volume sends

## The Diagnostic Signal

**Total reply rate is the primary deliverability indicator.**

If total reply rate drops below 2%, the first audit is infrastructure/copy — not offer, not targeting. A well-configured system with a weak offer will still see replies; a poorly configured system with a perfect offer will not.

## Relation to GTM Engineering

Cold email infrastructure is the [[GTM Engineering]] equivalent of a data pipeline: it's the unglamorous plumbing layer that must be right before the strategy layer matters. Most failed cold email campaigns fail at this layer, not at the copywriting or offer layer.

The speed limit constraint also explains why serious cold email operators look like infrastructure companies: dozens of domains, hundreds of inboxes, warmup SaaS subscriptions, and domain rotation schedules.

## See Also

- [[sources/anon-cold-email-systems-guide]] — primary source
- [[Cold Email Copywriting]] — the content layer that sits on top of this infrastructure
- [[Cold Email Personalization Problem]] — a higher-order problem that assumes the infrastructure is already correct
- [[GTM Engineering]] — cold email infrastructure as one implementation of GTM engineering
- [[sources/alexvacca-gtm-engineering-hire]] — empirical scale context: ColdIQ uses 4 ESPs simultaneously, dozens of domains
