---
title: "Sharded Growth Teams"
type: concept
tags: [org-design, team-structure, growth-marketing, horizontal-product]
created: 2026-07-15
updated: 2026-07-15
sources: [lukeharries-elevenlabs-growth-playbook]
---

# Sharded Growth Teams

*An organizational model that shards a company into per-product growth pods, each led by a mini-CMO, sitting under a separate horizontal layer of cross-product channel specialists.*

## Overview

Built at [[entities/elevenlabs|ElevenLabs]] to serve a genuinely horizontal, multi-product strategy — a single foundational technology (best-in-class audio AI) sold across a developer API, an enterprise conversational-AI platform, a consumer reader app, and a creative platform, none of which naturally compound into each other the way a single-ICP company's products would. [[entities/luke-harries|Luke Harries]] is explicit that this is *not* his default advice: for most companies, the better path is one ICP with multiple compounding products (he cites his own experience at PostHog — transcribed "Post Hoc" — as the archetype). Sharding is the adaptation this specific company needed because its GTM problem was multiple, disconnected go-to-markets running simultaneously.

## Key Properties / Characteristics

- **Horizontal layer**: channel specialists who serve every product pod — e.g., a head of performance marketing (ex-Shopify) and an SEO lead (ex-Canva).
- **Vertical layer**: one product growth lead per product line, functioning as that product's mini-CMO — owning activation, awareness, and all relevant metrics — with their own dedicated sub-team.
- Team sizes scale independently per pod: enterprise marketing alone scales to ~20 people by end of year; the mobile-app growth team runs 5–10.
- Growth pods are deliberately kept lean, which doubles as a guardrail against growth leads drifting into a shadow-PM role (see [[concepts/product-engineers-no-pms]]).

## How It Works

1. Identify each genuinely separate product/go-to-market line (in ElevenLabs' case: developer API, enterprise conversational AI, consumer reader app, creative platform).
2. Assign a product growth lead to each — responsible for that product's full growth funnel, acting like an internal CMO for it.
3. Build a horizontal team of channel experts (performance marketing, SEO, etc.) who plug into whichever pod needs them, rather than each pod hiring its own redundant channel specialists.
4. Staff each pod's sub-team to its own scale needs; pods are not required to be symmetric in size.

## Variants / Subtypes

- **Single-ICP compounding model (the default/safer alternative)**: one ICP, multiple products that cross-sell into each other, a single growth org serving all of them (the model Harries contrasts this against, using PostHog as the example).

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/lukeharries-elevenlabs-growth-playbook]] | ElevenLabs' enterprise marketing team alone will reach ~20 people by end of year; mobile growth team runs 5–10 | high (specific internal headcount figures from the practitioner running the org) |
| [[sources/lukeharries-elevenlabs-growth-playbook]] | Sharding "seems to be working really well" for ElevenLabs but the source explicitly does not recommend it as general advice | high (direct, self-qualified claim) |

## Contradictions & Open Questions

- No detail given on how budget is allocated or arbitrated *across* pods when they compete for the same horizontal specialists' time.
- Open question: at what company size/stage does sharding become necessary vs. premature? ElevenLabs adopted it only after multiple products already had independent traction — no guidance on doing this earlier.

## See Also

- [[concepts/growth-hiring-order]] — the sequence used to build out each pod from scratch
- [[concepts/product-engineers-no-pms]] — the guardrail that keeps pods lean rather than growing into shadow product-management functions
- [[concepts/gtm-engineering]] — related organizational-design concept already in the wiki (agent-per-vertical is the automated-agent analog of this human-team structure)
- [[sources/lukeharries-elevenlabs-growth-playbook]] — primary source
