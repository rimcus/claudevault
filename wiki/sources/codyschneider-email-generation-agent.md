---
title: "Build an AI Agent to Get Anyone's Email for Free"
type: source
tags: [cold-email, enrichment, email-finding, ai-agents, graphed, deliverability]
created: 2026-04-15
updated: 2026-04-15
sources: [codyschneider-email-generation-agent]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2046604872296841542"
source_type: x-post
---

# Build an AI Agent to Get Anyone's Email for Free

**Author:** [[Cody Schneider]] (@codyschneider)
**Published:** 2026-04-21
**Context:** Single post promoting [[Graphed]] as the platform to build this agent.

---

## Core Technique: Generate + Verify

Every business email follows a predictable pattern: `first.last@domain.com`, `f.last@domain.com`, `first@domain.com`, etc. Given a LinkedIn profile, an AI agent can:

1. **Generate** every plausible email variation for that person + domain
2. **Existence-check** each one using a cheap API (e.g., `mailtester.ninja`) — tests whether the mailbox actually exists
3. **Validate** the surviving emails with a deliverability tool (e.g., MillionVerifier)
4. **Cold email** the validated address

**Cost:** Near-zero. The email checker API is "extremely cheap"; the generation step is computational.

**Best for:** SMBs, where email naming patterns are more consistent and predictable.

---

## The Critical Caveat (from comments)

**@MrColdEmail (Sabo):**
> "Catch-all domains: around 30–40% of business domains are set up as catch-alls, meaning any combination will return 'valid' even if the address doesn't exist."

This is a significant limitation: for 30–40% of domains, the existence-check step produces false positives — the API says "valid" but the mailbox may not exist. This means bounce rates on catch-all domains remain high even after the generate-and-verify process.

**Implication:** The technique works cleanly for ~60–70% of domains. For the remainder, it's no better than an unverified guess — and sending to non-existent addresses on catch-all domains damages sender reputation.

---

## Relation to Enrichment Waterfall

This is a **zero-cost alternative** to the first pass in the [[Enrichment Waterfall]] — instead of paying Findymail/Prospeo to find emails, you generate and verify them yourself. The trade-off:

| Approach | Cost | Coverage | Catch-all Risk |
|----------|------|---------|----------------|
| Paid enrichment (Findymail) | ~$0.01–0.05/contact | ~50–60% (1st pass) | Handled by provider |
| Generate + verify (this technique) | Near-zero | ~60–70% (non-catch-all domains) | Requires separate handling |

For high-volume, cost-sensitive operations, generate + verify is compelling. For quality-sensitive campaigns (enterprise, high-ACV), paid enrichment with catch-all filtering may be safer.

---

## Entities Mentioned

- [[Cody Schneider]] — author
- [[Graphed]] — promoted as the platform to build this agent
- MillionVerifier — email validation tool (deliverability check)
- mailtester.ninja — cheap email existence checker API

## Concepts Touched

- [[Enrichment Waterfall]] — generate + verify as a zero-cost alternative to paid first-pass providers
- [[Cold Email Infrastructure]] — email validation is part of the deliverability layer
- [[GTM Agents]] — Schneider frames this as an agent to build, consistent with his broader GTM agents thesis

## See Also

- [[concepts/enrichment-waterfall]] — the broader context for this technique
- [[sources/codyschneider-gtm-agents]] — Schneider's full GTM agents framework
- [[entities/graphed]] — Schneider's product, promoted as the build platform
- [[sources/anon-cold-email-systems-guide]] — the infrastructure context; ZeroBounce for validation
- [[sources/salescaptain-linkedin-outbound-playbook]] — the paid waterfall (Findymail → FullEnrich → Apollo → ZeroBounce)
