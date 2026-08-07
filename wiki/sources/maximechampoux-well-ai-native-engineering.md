---
title: "SaaS Connection — Maxime Champoux (Well): Building an AI-Native Engineering Org"
type: source
tags: [ai-coding, engineering-culture, product-management, agent-orchestration, fintech, business-context-graph, french]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
author: "Maxime Champoux (interviewed by Alex Olivet)"
source_url: ""
source_type: podcast
---

# SaaS Connection — Maxime Champoux (Well): Building an AI-Native Engineering Org

**Author:** Maxime Champoux, CEO/co-founder of [[entities/well|Well]] (interviewed by [[entities/alex-olivet|Alex Olivet]], founder of Collect)
**Show:** SaaS Connection (French-language podcast)
**Language:** French — this summary is written in English per wiki convention; direct quotes below are translated
**Source:** transcript, no URL captured

## Core Thesis

[[entities/maxime-champoux|Maxime Champoux]] spent 15 years building fintech core infrastructure (first employee at [[entities/ibanfirst|iBanFirst]], then [[entities/qonto|Qonto]]'s Head of Products scaling a 2-person product org to 150) before founding Well, an AI agent platform that builds a unified "business context graph" for solopreneurs and small businesses. The episode is really two interlocking sources of alpha: (1) a detailed account of Qonto's Toyota-Production-System-inspired engineering culture, and (2) a granular, month-by-month account of what actually happened inside a 12-person team when it went from 7 shipped features/month to 100+/month between November 2025 and the recording date — including the specific plateau they hit, why it happened, and the agent-specialization fix that broke through it. This second half is the rarer material: most public accounts of "AI-native" engineering are aspirational; this one includes the failure mode (a quality plateau caused by agents that were "integrated but not assimilated" into the codebase) and the concrete fix (named, stable, domain-specialized agents with deliberately bounded context).

## Full Guide: Every Piece of Advice, By Topic

### 1. Career background — where the operating playbook comes from

- [[entities/maxime-champoux|Champoux]] joined [[entities/ibanfirst|iBanFirst]] as its first employee, in a period (~15 years before this recording) when "startup" wasn't yet a fashionable career path in France. His first job: build a Core Banking system from scratch, with no accessible playbook to benchmark against — took 2.5 years.
- Went on to specialize in payments APIs (pre-DSP2/open banking) at iBanFirst, then spent time at an early fintech (heard in the transcript as "Meljet"/"Medjet" — exact name unclear from the audio, later acquired by a company heard as "Med Gun" [low confidence on all three names]) as PM on the API, which is also where he first met [[entities/alex-olivet|Alex Olivet]] (who was doing growth there) roughly 8 years before this recording.
- Joined [[entities/qonto|Qonto]] at ~50 employees, recruited by co-founder Steve specifically for his dual expertise: he'd already shipped the first fully-online B2B account-opening flow at iBanFirst (a B2C-style onboarding experience for a legal entity with multiple shareholders, including a compliance "hack" — giving the customer their IBAN immediately post-onboarding, before full KYC/KYB validation completes, since the actual compliance risk is unauthorized *payment* before validation, not merely holding an account number) — and his Core Banking build expertise. Qonto had inherited its onboarding flow from iBanFirst and needed both pieces at once.
- At Qonto, rebuilt the Core Banking system in 6 months (vs. 2.5 years at iBanFirst) with a small team — his framing: "speed and quality are not a trade-off."

### 2. Why companies bring Core Banking in-house

Qonto initially ran on a banking-as-a-service provider (heard in the transcript as "Trésor" — likely Treezor, a real BaaS provider historically used by early Qonto [medium confidence on the name mapping]; not a wiki entity page). The reasoning for eventually internalizing it, generalized as advice: a centralized BaaS provider serves multiple clients simultaneously and may not move at your speed or in your direction — its roadmap and quality bar are shared across its whole client base, not owned by you. Champoux draws a direct parallel to a tension he sees playing out currently between a company heard as "Penel" (possibly Pennylane [low confidence]) and its BaaS provider Swan — the same dependency dynamic recurring in the market [neither a wiki entity page]. The other driver is margin: card-interchange revenue is the primary economic driver of a Core Banking business, and every day spent still relying on a third-party provider is margin left on the table — a direct incentive to launch in-house banking as fast as possible.

### 3. The Toyota Production System applied to software ("Qontoway")

See [[concepts/toyota-production-system-for-software]] for full detail. Qonto's internal engineering culture, nicknamed "the Qontoway," is explicitly modeled on the Toyota Production System: software is treated as an assembly line (think: building a Toyota Yaris), where each contributor — backend, frontend, PM — has a specific task, in a specific order, and the PM's job is to specify the "vehicle concept" and each station's task on the line, then keep the line accelerating without sacrificing quality. Core mechanics: a zero-bugs-in-production standard; an Andon-cord-style stop-the-line practice (pull the cord the moment a defect is spotted — the line halts immediately, the manager comes to investigate with you, and production doesn't resume until the root cause is found and fixed); continuous improvement built around root-cause analysis, not just symptom patching; and an explicit rule to fix a problem immediately rather than keep shipping around it.

### 4. Scaling a product org — headcount, ratios, and the pre-AI ceiling

- Qonto scaled from ~50 to 1,600 employees and (per Champoux) ~25,000 to ~600,000 SMB customers during his ~7 years there [figures as stated by the practitioner; not independently verified].
- Following a ~$500M raise (Tiger Global, per Champoux, ~4 years before this recording [unverified against public record]), the explicit strategic goal was defensibility through velocity — shipping more functionality than competitors, framed as widening the company's competitive "moat."
- Concretely this meant recruiting 36 product managers in 12 months, scaling the product org to ~150 people (roughly 50 PMs plus product designers, product marketers, and UX writers), at a PM-to-engineer ratio of roughly 1:8.
- Champoux's framing of the pre-AI world: shipping velocity had exactly one lever — the number of engineers you could parallelize. Codebase size itself functioned as a competitive moat (a 2-million-line codebase is a real barrier to a competitor trying to replicate it by hand).
- Corroborating data point relayed secondhand: a podcast guest heard as "Romain" at OpenAI (possibly Romain Huet [low confidence]; not a wiki entity page) reportedly said Codex had shifted his own PM-to-engineer ratio from 1:6 to 1:2, and that he wouldn't be surprised if it eventually inverted — needing more PMs than engineers.

### 5. What changed in November 2025 — the actual inflection point

Champoux dates the real paradigm shift specifically to November 2025 (associated with the release of Claude Opus 4.5): the shift from "AI-augmented engineer" (still meaningfully bottlenecked on human-typed lines of code) to a world where **intent is what gets coded, not lines of code**. He frames both the pre-November "headcount is the moat" world and the "codebase size is the moat" world as now-obsolete relative to this shift — though he notes Qonto (which he'd left by then) has very likely accelerated significantly since, using the same underlying capability shift at much larger scale.

### 6. Well — the product, and the problem it actually solves

See [[concepts/business-context-graph]] for full detail. Well's mission (carried over directly from Champoux's stated motivation at Qonto): accelerate entrepreneurship by reducing the administrative burden on small-business owners, freeing time for the actual business. The product started narrower than it ended up: browser + email + WhatsApp agents that automatically retrieve missing invoices for monthly bookkeeping close, cutting a 2–5 hour manual task to about 2 minutes. Building that surfaced a harder problem — the agents lacked *context*: to know which invoices were actually missing, you need the bank transaction feed, the existing invoice history, and a categorization layer (small transfers or internal transfers don't need justification; most transactions do). Pulling that thread led to building a general-purpose **business context graph**: a unified data model spanning bank transactions, suppliers, customers, contact points, accounting, and subscription/billing management — explicitly modeled on how Attio built a unified data model for the CRM category (not a wiki entity page), but generalized beyond CRM into something functioning as an ERP layer for businesses too small to ever buy a real ERP or build a data warehouse.

### 7. The connector strategy — MCP-first, self-extending

Well's technical approach to pulling scattered SaaS data together, in priority order: (1) use an existing MCP connector if one is available in public MCP directories; (2) if none exists, generate one from the tool's API documentation; (3) if there's no API documentation either, fall back to a Chrome extension performing actions via vision models or scripts. Critically, connectors are **not** pre-built speculatively for every SaaS tool that exists — they're built reactively, triggered by actual customer data (a detected bank transaction or an email referencing a tool the customer uses that Well doesn't yet support), which then triggers the same MCP → API-doc → browser-fallback waterfall to close the gap. Champoux frames this explicitly as **not** trying to pre-integrate with the entire SaaS universe up front.

### 8. The team-wide AI-coding transition, month by month

See [[concepts/ai-native-engineering-team]] for full detail. November 2025: the team (12 people — 8 engineers, designers, brand designer, Champoux himself, later a growth engineer) was shipping ~7 features/month. Within the first month of going "100% team codes" (everyone, including designers and Champoux, using Claude Code directly), output doubled to ~14/month. By February, marginal-gains compounding (see below) had pushed this to somewhere in the 40s/month. The team hit a **plateau at 40–50 features/month through March–April**, which they diagnosed and broke through (see below), reaching 100+/month by the time of this recording — with the same 12-person team throughout.

Two explicit conditions were required for the "everyone codes" transition to work at all:
1. **Bounded permissions, defined as skills**: non-engineers are explicitly not allowed to touch backend or system architecture — only frontend, and only with the domain owner's validation.
2. **Full team buy-in ("change management")**: the 2x result in month one only happened because the whole team committed to going "100%," not as a partial pilot.

### 9. Why the design/Figma relationship inverted

See [[concepts/design-code-inversion]]. For roughly the last decade, Figma functioned as the source of truth upstream of code: designers spec the experience in Figma, engineers build code to match it, and future iterations start again from Figma. Well now runs this in reverse: **code is the source of truth**, and Figma has become something closer to a "slave" artifact the team can no longer realistically keep in sync, because code now moves faster than Figma can be updated to track it. The designer's role has moved downstream in the production line — instead of specifying the feature up front, the designer now receives a raw, functional feature and does the finishing work: reconciling it with the design system, ensuring components are properly created, and polishing the UX.

### 10. The "1% marginal gains" tooling discipline

See [[concepts/marginal-gains-1-percent]]. Explicitly borrowed from cycling — Dave Brailsford's marginal-gains methodology at British Cycling/Team Sky (improve sleep, nutrition, equipment by 1% each, compounding into outsized aggregate performance) — applied to the AI-coding tool stack. The team's working rule from January onward: **look for a 1%-per-day improvement to the tooling.** Concretely this meant small automations and reusable "skills," shared with the whole team via pull requests the moment anyone believed a change would produce even a marginal gain. This compounding discipline is what pushed velocity from the initial 2x (Nov→Dec) up toward the 40s/month by February.

### 11. Diagnosing the plateau: "integration" vs. "assimilation," and code patina

See [[concepts/agent-specialization-context-window]] for full detail — this is the most novel material in the source. At the 40–50/month plateau (March–April), the team paused shipping velocity deliberately to instrument and diagnose the problem, using **OpenTelemetry (OTel)** to capture everything typed into the team's terminals across Claude Code and Codex sessions — initial prompts, which documents got pulled into context, and which agents were invoked — specifically to root-cause quality regressions.

The diagnosis: a feature could be **integrated** (it works in isolation; its own automated tests pass) without being **assimilated** (it doesn't actually account for the rest of the system — it can silently break existing behavior). The root cause of failed assimilation is what Champoux calls **"code patina"** — the accumulated, often non-obvious detours in how code is actually written for reasons that aren't visible from the code itself. An agent unaware of a specific patina-driven detour will take the "straight line" (the obviously simpler implementation) instead — and that straight line is often exactly the path that reintroduces a previously-fixed regression.

**The fix**: it isn't enough to document the reasoning behind a patina detour — the agent executing in that part of the codebase also has to be *specialized* enough that its own cognitive load (context window) isn't overwhelmed trying to hold the entire system in mind at once. Well settled on 8 **named, stable** specialized agents mapped to production-cycle roles (e.g., a design specialist, a data-model specialist, a connectors specialist, a design-system/table-generation specialist), each launched with a **guaranteed baseline context** (its own domain documentation, expandable with adjacent documentation as needed for a given task). When building a feature, an **orchestrator agent** interprets the feature's intent and deploys the correct specialized agents for the job. The explicit rule: never let a generic, unspecialized agent execute specialized work, purely for quality reasons — even though a generic agent *could* technically attempt it (the same way a human could technically attempt a task outside their specialty), doing so reliably produces lower quality because it lacks the specific context.

**The generalizable heuristic for when you need to specialize at all**: it comes down to context-window capacity relative to cognitive load. If a generic agent can hold your entire documentation and/or codebase inside its context window, you don't need to specialize (or need only light steering). Once the material needed to do a task well exceeds what a single context window can responsibly hold, that's the trigger to split into named, bounded, specialized agents — a rough proxy for this threshold is documentation size / lines of code, the same variable that historically forced human teams to split into specialized squads as a product surface grew (Champoux draws this parallel directly from his own experience scaling Qonto's product org from 2 to 150 people).

A second, complementary practice from the same period: engineers began **personifying** quality-review agents — e.g., one engineer built a "Claude as Maxime" persona that reviews every PR the way Champoux himself would. Every time that review surfaces a quality gap (his example: a missing translation), the fix isn't just to patch the instance — it's to create a new reusable **skill** so that entire class of defect can never recur, and to fold it into the shared pipeline so it benefits the whole team rather than just the engineer who found it.

Also in April: documentation was moved from an external tool (Notion) directly into the codebase itself, consolidating the source of truth for both humans and agents in one place.

### 12. The roadmap/PM bottleneck, and reshaping the Double Diamond

See [[concepts/roadmap-abstraction-shift]] for full detail. With output scaling into the hundreds of features/month and only one person (Champoux) doing product work, product definition itself became the bottleneck. The classic Double Diamond framework (diverge/converge to a concept, then diverge/converge again with engineering into a 4–6-week feasibility-scoped spec) stopped making sense once a "4–6 week" scope could be executed in about 2 hours — there was no longer a reason to arbitrarily cut a feature's scope down to fit an obsolete time-box. The team's response: move back one level of abstraction. Champoux now works from **concept-level vision** (a 6–12 month horizon) rather than detailed specs; the engineer takes that concept and produces their own (more technical) implementation plan — typically a 1–3 day exercise — against a rougher, "brute" version of the product, which the designer then polishes downstream (per §9).

Champoux's own briefing style is explicitly **black-box**: for a given feature he defines desired inputs, desired outputs, and the desired experience, and deliberately does not specify the internal "how" — that's delegated to the engineer and their agents. What *can* now be heavily automated is the concept-diverging research phase itself: competitor analysis, pattern identification (both in the market and in Well's own codebase, to reason about how a new pattern should be assimilated), and light market intelligence on pricing/positioning — a chain of skills that used to take about two weeks of manual research and now takes about one hour, at what Champoux says is *better* quality than the old two-week process, not just faster.

The deliverable format also evolved: Champoux used to hand off low-fidelity ASCII wireframes; he now delivers high-fidelity **HTML wireframes rendered live using the team's actual Storybook design-system components** (so the mockup is built from real UI building blocks, not approximations), described using a Gherkin/BDD-style Given-When-Then format for precisely specifying dependencies and edge cases — effectively a TDD-style spec for a feature that hasn't been built yet.

### 13. How the team stays current, and what it reads

Well maintains dedicated Slack channels for sharing AI/productivity findings and interesting design/competitive-intelligence discoveries — deliberately **not automated**, kept organic, so anyone can revisit an earlier post later and decide whether it's worth digging into for their own specific problem. Champoux cites Daniel Kahneman's *Thinking, Fast and Slow* (System 1/System 2) as an influential general decision-making framework the team draws on — not AI-specific, but a mental model they lean on. Primary day-to-day sources for staying current: X (Twitter) and LinkedIn.

### 14. Business model and go-to-market detail

Well is free to use until September (year unspecified in-transcript, presumably 2026). A distinctive GTM/product detail: Well's own MCP connectors are exposed directly inside Claude — meaning a user can connect Claude to their own unified business context through a single Well MCP channel, with authentication persisting across sessions, rather than having to build or maintain individual point integrations themselves. Champoux publishes LinkedIn articles roughly 1–2 times per month, generally deep, thought-leadership-style write-ups of what the Well team is learning while building the product; now that Well has launched publicly, this is starting to include some direct product communication as well.

## Notable Quotes

> "Speed and quality are not a trade-off."

> "It's not lines of code anymore — it's intent that gets coded."

> "You want assimilation, not just integration. Integration is fast; assimilation is what lets you go far."

> "If I give you a task outside your specialty, you're capable of doing it — but you'll take shortcuts, because you don't know the codebase's patina."

## Entities Mentioned

- [[entities/maxime-champoux|Maxime Champoux]] — CEO/co-founder, Well; prior Head of Products at Qonto; first employee at iBanFirst
- [[entities/alex-olivet|Alex Olivet]] — host, SaaS Connection; founder of Collect
- [[entities/well|Well]] — Champoux's AI business-context-graph startup for SMBs
- [[entities/qonto|Qonto]] — French neobank; Champoux's employer for ~7 years, scaling 50→1,600 employees
- [[entities/ibanfirst|iBanFirst]] — fintech; Champoux's first employer, first Core Banking build

## Concepts Touched

- [[concepts/toyota-production-system-for-software]] — new
- [[concepts/business-context-graph]] — new
- [[concepts/ai-native-engineering-team]] — new
- [[concepts/design-code-inversion]] — new
- [[concepts/agent-specialization-context-window]] — new
- [[concepts/marginal-gains-1-percent]] — new
- [[concepts/roadmap-abstraction-shift]] — new
- [[concepts/schema-governed-llm-behavior]] — touched (Well's in-codebase documentation + skills mirror this wiki's CLAUDE.md concept, applied to production engineering rather than GTM)
- [[concepts/gtm-engineering]] — touched (treating engineering itself, not just GTM, as an agent-orchestrated pipeline)
- [[concepts/data-warehouse-for-ai]] — touched (Well's business context graph is this wiki's data-warehouse-for-ai thesis applied to SMBs who can't afford a real data warehouse)

## My Notes

This is the wiki's first source on **AI-native software engineering process itself** — distinct from both the cold-email/GTM-agent core and the general growth-marketing layer added by the ElevenLabs source. It's also the most concrete, falsifiable account in the wiki of what breaks when a team pushes AI-coding velocity hard (the integration-vs-assimilation plateau) and what specifically fixes it (named, stable, context-bounded specialized agents plus an orchestrator) — this generalizes directly to [[concepts/schema-governed-llm-behavior]] and [[concepts/gtm-agents]]' existing "agents write their own skill files" pattern, but applied one layer down, to the software itself rather than to marketing workflows. Worth flagging: several proper nouns in this transcript are ambiguous due to French auto-transcription artifacts (the earlier employer "Meljet"/"Medjet," the BaaS provider "Trésor," the company "Penel," the OpenAI podcast guest "Romain," and even Well's own name appearing once as "Weal") — all flagged inline with confidence markers; none of the core operational claims (ratios, timelines, the plateau/fix mechanism) depend on getting these names exactly right.

## See Also

- [[concepts/schema-governed-llm-behavior]] — CLAUDE.md-style persistent memory, the closest existing wiki concept to Well's in-codebase skills/documentation
- [[concepts/gtm-agents]] — "agents write their own skill files" pattern, the GTM-side analog to this source's engineering-side agent specialization
- [[concepts/data-warehouse-for-ai]] — the data-centralization thesis, here applied to SMBs via a business context graph instead of a company-scale warehouse
- [[sources/lukeharries-elevenlabs-growth-playbook]] — this wiki's other "no-PM, product-engineer-owned roadmap" source; useful contrast in how two different companies reorganized around AI coding capability
- [[concepts/product-engineers-no-pms]] — direct parallel: both sources describe PM work compressing/merging into engineering as AI coding capability increases
