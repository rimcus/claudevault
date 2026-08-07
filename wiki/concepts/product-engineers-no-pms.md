---
title: "Product Engineers Instead of PMs"
type: concept
tags: [org-design, product-management, engineering, ai-coding, hiring]
created: 2026-07-15
updated: 2026-07-15
sources: [lukeharries-elevenlabs-growth-playbook]
---

# Product Engineers Instead of PMs

*ElevenLabs runs with no dedicated PM function — engineers own the roadmap end-to-end, on the thesis that AI-assisted coding is collapsing the traditional PM/engineering/marketing split.*

## Overview

[[entities/luke-harries|Luke Harries]] describes [[entities/elevenlabs|ElevenLabs]]' explicit choice not to hire product managers. The underlying thesis: engineers who build the product, and who talk directly to users, generate better-grounded ideas than a PM relaying secondhand feedback — and collapsing ideation → shipping → analysis into one person removes hand-off latency and permission-seeking friction. This connects to the same "roles merging" trend behind [[concepts/growth-hiring-order]]'s growth-engineer hire and the broader growth-lead role (which absorbs what would otherwise be split across PM + marketing).

## Key Properties / Characteristics

- Engineers own the full loop: idea → wireframe → ship → analyze results — without needing anyone else's permission to move to the next step.
- Growth leads partner with an engineering lead per product but do not manage product scope themselves.
- A specific hiring filter ("the product challenge") screens for engineers who can be trusted with this scope.
- Explicitly gated by hiring quality: "if you hire great engineers, they just don't need [a PM]."

## How It Works

**The product challenge (hiring filter).** Every engineering candidate is given a hypothetical product and asked to:
1. Work out what features to build — researching real competitors and reasoning from an imagined customer's perspective (not guessing in the abstract).
2. Turn that into wireframes/mockups (e.g., in Figma).
3. Design the system architecture — backend structure, API design.

Only candidates who clear a separately-screened strong coding bar *and* this product-challenge loop are hired — the combination is what lets ElevenLabs trust an engineer with full-stack product ownership instead of routing decisions through a PM.

**The growth-team guardrail against scope creep.** Growth/product-growth leads are deliberately kept small and lean (see [[concepts/sharded-growth-teams]]) specifically so there isn't slack time for them to start meddling in engineering decisions like wireframes or running large numbers of user interviews — that discipline lives with engineering, not growth.

## Where PMs Go Next (per Harries)

Two predicted destinations as the traditional PM role dissolves:
1. **Merge into growth** — combining the PM function with marketing into the single product-growth-lead role described in [[concepts/sharded-growth-teams]].
2. **Move into product engineering** — upskilling via AI coding tools (Cursor, [[entities/lovable|Lovable]]) to ship full end-to-end features solo, becoming "somewhat technical" product engineers themselves.

## AI-Generated Code at ElevenLabs

- Roughly 60–70% of ElevenLabs' core engineering code is now AI-generated.
- Harries personally writes ~20% of his own code by hand; the rest is prompted through Cursor, mostly for growth-facing features layered on top of the core product.
- Explicit exception: **research engineering stays entirely human-written.** Reasons given: the codebases are unusually sensitive, and research work is a fundamentally different discipline from standard engineering — not a candidate for LLM-assisted authorship at ElevenLabs currently.
- Context: at the time of ElevenLabs' initial breakout to a ~$1B valuation, Harries estimates roughly half the company's enterprise value was attributable to the core audio model itself (built by co-founder Piotr/"Peter") — underscoring why that specific code stays fully human-authored even as the rest of the codebase shifts to AI generation.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/lukeharries-elevenlabs-growth-playbook]] | ElevenLabs has no PM function; engineers own the roadmap directly | high (direct organizational claim from the practitioner) |
| [[sources/lukeharries-elevenlabs-growth-playbook]] | ~60–70% of core engineering code is AI-generated; ~20% of Harries' own code is hand-written | high (specific figures, though self-reported and not independently audited) |

## Contradictions & Open Questions

- No detail on how ElevenLabs handles cross-product roadmap conflicts without a PM layer to arbitrate priorities between engineering teams.
- Open question: does the "product challenge" hiring filter scale to senior/staff engineering hires the same way, or is it described specifically for early-career candidates?

## Convergent Evidence: Qonto/Well (Champoux)

[[sources/maximechampoux-well-ai-native-engineering]] documents an independent version of the same underlying trend from a different company and a different angle: rather than eliminating the PM role outright, [[entities/maxime-champoux|Maxime Champoux]] describes the PM's own work compressing upward in abstraction (see [[concepts/roadmap-abstraction-shift]]) as engineers, now aided by specialized coding agents, absorb the detailed-spec-writing work a PM used to do. A secondhand data point in that source (an OpenAI podcast guest reportedly moving from a 1:6 to a 1:2 PM-to-engineer ratio, speculating it could eventually invert) is directionally consistent with Harries' thesis here, though from an unrelated company.

## See Also

- [[concepts/sharded-growth-teams]] — the org structure this guardrail protects
- [[concepts/growth-hiring-order]] — the growth-engineer hire is the other half of the "roles merging" trend
- [[concepts/gtm-engineering]] — existing wiki concept on treating GTM as code-driven infrastructure; parallel thesis applied to product management here
- [[concepts/roadmap-abstraction-shift]] — the Well/Champoux parallel: PM role compresses upward rather than disappearing
- [[sources/lukeharries-elevenlabs-growth-playbook]] — primary source
- [[sources/maximechampoux-well-ai-native-engineering]] — convergent independent source
