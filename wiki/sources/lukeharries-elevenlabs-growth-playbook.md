---
title: "The $3.3B Growth Engine Behind ElevenLabs"
type: source
tags: [growth-marketing, launches, video-marketing, saas, product-led-growth, team-structure, consumer-and-enterprise]
created: 2026-07-15
updated: 2026-07-15
sources: [lukeharries-elevenlabs-growth-playbook]
author: "Luke Harries (interviewed by Harry Stebbings)"
source_url: ""
source_type: podcast
---

# The $3.3B Growth Engine Behind ElevenLabs

**Author:** Luke Harries, Head of Growth at [[entities/elevenlabs|ElevenLabs]] (interviewed by [[entities/harry-stebbings|Harry Stebbings]])
**Show:** 20VC / 20 Growth
**Source:** transcript, no URL captured

## Core Thesis

[[entities/luke-harries|Luke Harries]] built ElevenLabs' growth function from three junior generalists to a sharded, channel-specialist organization while the company scaled toward a $3.3B valuation. The episode is a practitioner's field guide rather than a single big idea: how to structure growth teams under a horizontal, multi-product strategy, how to run a launch that reliably gets 200K–700K views, which video format to use and when, why CAC:LTV is the wrong ratio and CAC:payback-period is the right one, why ElevenLabs runs with no PMs, and a set of sharp, quotable positions on counter-positioning, founder brand, SEO's half-life, and paid marketing's correct sequencing (never before PMF). Almost every answer is opinionated and falsifiable — this is the value of the source.

## Full Guide: Every Piece of Advice, By Topic

### 1. Horizontal product strategy (and why it usually shouldn't work)

- Standard advice is a tight ICP with products that compound into each other — Harries cites his prior employer PostHog's model as the archetype (transcribed as "Post Hoc"/"Postdog" — likely PostHog [low confidence on exact name]): one ICP (product engineer), multiple cross-selling products (analytics, session recording, feature flags), each new product an additional entry point.
- ElevenLabs has none of that natural compounding. Its foundation is a single horizontal capability — best-in-class audio AI (text-to-speech, speech-to-text, sound effects, voice isolation) — sold as an API to wildly different buyers: developers building voice agents, commuters wanting audiobooks read aloud, enterprises, and a from-scratch consumer reader app and creative platform.
- It works anyway, per Harries, because (1) the underlying model is genuinely best-in-class so demand arrives unprompted across every vertical, (2) that demand funded hiring "founder-type" owners for each new product line, and (3) each product got its own dedicated team rather than being bolted onto a shared roadmap.
- His explicit caveat: **"I'm not sure I'd recommend it"** — this only works if you already have a horizontal, category-defining core technology. Founders with a normal single product should still choose one ICP and compound around it.

### 2. Sharded growth team structure

See [[concepts/sharded-growth-teams]] for the full breakdown. Summary: a **horizontal layer** of channel specialists (ex-Shopify head of performance marketing, ex-Canva SEO lead) sits above **vertical pods**, one per product line, each led by a product growth lead who is effectively that product's mini-CMO (owns activation, awareness, metrics) and runs their own dedicated sub-team. Enterprise marketing alone scales to ~20 people by end of year; the mobile app growth team runs 5–10.

### 3. The growth hiring order

See [[concepts/growth-hiring-order]]. Sequence: (1) one generalist growth marketer who understands the product deeply and owns messaging through channels end-to-end — never split this into a product marketer *or* a channels person alone, each fails without the other; (2) a front-end-leaning growth engineer who builds SEO pages, mini-tools, and automated outreach; (3) a motion designer, brought in-house as soon as launches need to move fast; (4) additional channel specialists only once a channel has already shown organic signs of life — ElevenLabs' own regret is under-staffing proven channels (see affiliates, below).

### 4. Launch strategy — the tiered playbook

See [[concepts/launch-playbook]] for full detail. Three tiers (major model/product = Tier 1, notable feature = Tier 2, changelog-only = Tier 3). For Tier 1: nail messaging first (audience, KPIs, one primary value prop repeated everywhere + secondary props), then build assets in a fixed order — tweet thread first, launch video second (motion design preferred for Tier 1), blog post third (technical depth + SEO/backlinks) — then distribute everywhere simultaneously and coordinate an internal Slack "amplification" push where the whole company reshares within minutes of going live, specifically to trip the social algorithms' early-engagement signal. Results: 200K–700K views per major launch.

### 5. Video strategy for growth

See [[concepts/growth-video-strategy]]. Three formats — motion design (safe default, abstract, good for complex products), founder-led talking head (risky, ego-prone, cites Superhuman's 5-minute founder-led launch video as a specific miss — "by the time he's walked down the staircase, you've moved on"), and screen-share (fast, best for technical audiences who want to see the product itself; recommends the tool Screen Studio). The operating rule: **assume nearly all viewer attention lives in the first 30 seconds** — front-load the value prop regardless of total runtime. Bring motion design in-house as soon as possible; test the hire cheaply first via a $5–10K project-based freelancer engagement before committing headcount — the organic reach of one launch (200K–700K views) would cost far more bought as paid media.

### 6. Distribution mechanics

- **Cross-post everywhere**, even to channels where your audience is thin today (X, LinkedIn, Bluesky, Threads, Product Hunt, Reddit, Hacker News) — you reach people who simply prefer other platforms, and because competitors ignore the smaller channels, you can own them cheaply.
- **X and LinkedIn carry different audiences** for ElevenLabs specifically: X skews creator/developer, LinkedIn skews future-employee/partner/enterprise — but content is written to work for both.
- **Tweet-thread mechanics**: first word must signal a launch ("Introducing," "We're excited to..."); first tweet = one clean line naming exactly what's launching; then a space, then a bullet list or short paragraph on secondary value props; attach the launch video to the first tweet. Never put the link in the first tweet — Twitter/X actively downranks it (per Elon Musk's own statement) — put the call-to-action and link in the second-to-last tweet of the thread, and make that tweet itself strong, since threads get algorithmically truncated to first + last two tweets in most feeds.
- **Manually seed your own network** for every launch: pull every person you've ever emailed (five years of Gmail can mean 3,000+ contacts), every Twitter follower, every LinkedIn connection, and personally DM a chunk of them to boost the launch. This is explicitly framed as "be shameless" and "do things that don't scale" — Stebbings independently confirms this from growing 20VC: personally DM'd his first 50,000 Twitter followers, cross-promoting the newsletter in each DM, ~15 minutes/day.
- **Algorithmic mechanism stated directly**: 30–40 likes within the first 5 minutes of a post reads to the platform as a signal to promote it to a wider audience — this is why the amplification/DM steps above exist; they aren't vanity, they're the unlock for organic reach at scale.
- **New in-house creator hire**: ElevenLabs hired a creator whose sole job is TikTok/YouTube/Instagram Shorts, after noticing his own ElevenLabs-branded videos outranked ElevenLabs' own official channel by views — the hiring signal was organic outperformance, not a resume.

### 7. Blog posts and SEO are not dead — but the form is splitting

See [[concepts/seo-mini-tools]]. Long-form blog SEO is judged likely to decline (though not dead yet — Zapier still gets 70%+ of its SEO traffic from blog content) as AI answers absorb more query volume directly. What Harries is confident survives at least ~5 years: **"two pages"** — single-purpose mini-tools (e.g. a working text-to-speech box that ranks #1 for "text to speech Spanish") that require actual product engineering to build, not just words, so an LLM can't trivially replicate or replace them as a search result. The same mini-tool logic solves the B2B enterprise-trial problem: buyers won't commit without trying something, but you can't give away a whole enterprise product for free — so a growth engineer's job is to expose small, self-contained slices of real value outside the login wall (ElevenLabs' homepage is built almost entirely of these free-to-try text boxes), enough for a prospect to hit a "wow" moment fast without giving away the whole product.

### 8. CAC, payback period, and North Star metrics

See [[concepts/cac-payback-period]]. Headline claim: ElevenLabs tracks **CAC-to-payback-period, not CAC-to-LTV**, because LTV is too unstable and retroactive to steer by — cats (CAC) swing quickly and LTV can expand unpredictably as customers adopt more product lines over time. Payback targets vary by product: ~12 months for lighter/self-serve, 24 typical, up to 36 months for large multi-year enterprise contracts. If a channel beats its target ratio, the instruction is not incremental spend increases but to **"grow as quickly as you can"** — a good ratio is treated as explicit permission to prioritize speed. If a channel is below target, that's an acceptable deliberate bet as long as it's conscious (e.g., accepting losses for two years on a new product thesis). Individual-channel CAC does tend to rise over time (audience saturation, less-defined ICP at the margin) but **blended company CAC can hold flat or fall** as new channels are added, conversion/activation improves, and cheap entry products (consumer) feed users upward into pricier tiers (creator, enterprise). North Star for the enterprise motion specifically: **marketing-sourced SQLs** (lead identified by marketing → booked call with an SDR → SDR confirms qualified) — not blended pipeline dollars. Enterprise/organic channels are evaluated with deliberately fuzzy, longer-horizon attribution — e.g., comparing lift in leads for a geo running a coordinated multi-channel push (billboards, podcasts, newsletters, on-the-ground events) against a comparable control geo — rather than isolating any single channel's ROI.

### 9. Enterprise vs. consumer retention — the metric people get wrong

- Enterprise NRR is clean: sign one seat, expand seats, watch net revenue retention on the account climb past 100% even if individual users inside the account churn — the unit that matters is the account, not the seat.
- Consumer/prosumer retention (e.g. individual users on a tool like [[entities/lovable|Lovable]]) commonly runs *below* 100% at the individual level — and Harries argues that's fine to accept, because the natural virality of consumer products (a user builds something, shares it, and pulls in more signups) means the *account-level or cohort-level* NRR, once organic referral growth is counted, can end up higher than the raw per-seat number suggests. The mistake is judging consumer retention by enterprise-style seat-retention math.

### 10. Is Gen-AI company revenue "real"?

Harries' position: if the product solves a real problem and retention holds, the revenue is real, full stop — including cases hitting $6–10M ARR inside a single year. His pointed critique of VCs: many are still under-investing relative to the growth rates they're observing, comparing the current moment favorably to the COVID-era "invest fast" window, on the logic that model capability keeps compounding and unlocks genuinely new product categories. Side observation: the competitive landscape has gone from 2–3 credible players per category a few years ago to 10–15 today, making winner-picking harder even though most of the pack shows real traction.

### 11. Why ElevenLabs has no PMs

See [[concepts/product-engineers-no-pms]]. Thesis: engineers who build the product should own the roadmap outright — idea, wireframe, ship, analyze — because they're the ones actually talking to users and have the context to have better ideas, and removing the PM handoff removes a permission-seeking bottleneck. Guardrail against growth leads sliding into a shadow-PM role: keep growth teams deliberately small and lean so there's no slack time to meddle in engineering decisions. Hiring bar: every engineering candidate goes through a three-step **product challenge** — (1) research competitors and derive features as a hypothetical customer would, (2) turn that into wireframes/Figma, (3) design the system architecture (backend, API design) — on top of a separately-screened strong coding bar. Where Harries thinks PMs go next: either merge into the growth role (PM + marketing = product growth lead), or move into product engineering by upskilling on tools like Cursor or [[entities/lovable|Lovable]] to ship full features solo.
- AI-generated code data point: roughly 60–70% of ElevenLabs' core engineering code is now AI-written; Harries personally writes only ~20% by hand himself (he prompts Cursor for the rest, mostly growth-facing features layered on top of core product). Explicit exception: research engineering stays entirely human-written — the codebases are unusually sensitive and it's a fundamentally different (research, not engineering) discipline.

### 12. Counter-positioning

See [[concepts/counter-positioning]]. Definition given directly: take a competitor's core positioning claim and use its literal opposite as your own core strength. Canonical example cited: Ramp vs. Brex — Brex's positioning was card rewards/points; Ramp reframed points as a waste of money and repositioned around redirecting that value into software savings instead, successfully making "points" itself look like a liability across the whole category. Second example: TBPN positioned as the opposite of the All-In podcast on nearly every axis simultaneously — ads vs. no-ads, pro-tech vs. media's anti-tech drift, raw/live vs. polished, and smart/formal dress vs. hoodie tech-bro style. Harries frames this as "genius marketing," not a knock. Stebbings adds his own unprompted example: 20VC's short/concise format was itself a counter-position against long-form (3-hour) podcasting.

### 13. Founder brand

See [[concepts/founder-brand-strategy]]. Core guidance: pick the channel format the founder is *genuinely and sustainably* excited by, don't force one that "should" work. It's a 10–20 year commitment, not a campaign, and forcing a mismatched channel risks optimizing for the wrong signal (like-count dopamine) and becoming a distraction from running the company. ElevenLabs example: co-founder Mati is strong at in-person keynotes/fireside chats and leans fully into that; he isn't naturally active on X, so the company doesn't force him there — other people (including Harries) carry the public online content load instead. Bad-press caveat: **"no such thing as bad press" explicitly does not hold once you're selling to enterprise** — cited example: a company ("Cheat on Anything," raised $5.3M) whose founder-led growth hook is bragging about using the product to cheat and land job offers at Amazon/Palantir/Google; brilliant top-of-funnel virality, but it plants a trust flag that will actively work against the company the moment it needs enterprise sales teams to see it as a trusted partner. Read: authentic founder brand tied to a genuine belief can survive scrutiny even when controversial ([[entities/bryan-johnson|Bryan Johnson]]/"Don't Die," discussed in the quickfire round, is judged authentic because he demonstrably believes in the longevity mission); a brand built on a bit or gimmick doesn't get the same grace, and reversing an already-locked brand identity later is exceptionally hard (analogy given: Calm trying to shed being "the meditation app").

### 14. Competition philosophy

Two valid approaches, per Harries: (a) the YC-style approach — ignore competitors, talk only to customers, build an incredible product; good for product development specifically. (b) counter-positioning as marketing strategy (see above) — good when an incumbent's positioning has calcified into an assumed market norm you can invert.

### 15. Quickfire round — rapid-fire positions

- **Most expensive early-founder mistake**: running paid marketing before product-market fit. Without PMF you burn engineering time optimizing funnels/creative/rankings that don't matter yet — build an incredible product and run great launches first, and that alone is usually enough to reach initial PMF for most B2B/prosumer products. Caveat: pure consumer-distribution-into-B2B plays are different — if the product is exceptional you can staff a sales team onto it and scale distribution later, whereas consumer often needs earlier paid spend because distribution itself (not sales capacity) is the constraint.
- **Most underrated growth channel today**: organic LinkedIn and Twitter/X — the bar to stand out is low ("you're competing against Freddie from Deloitte who got a promotion"), so genuine, well-written content clears it easily.
- **Most "polluted"/overrated channel**: LinkedIn ads — CPMs are high, and it's disproportionately used by exactly the long-sales-cycle enterprise sellers who'd get more value investing that same time into excellent organic content instead.
- **#1 advice for someone starting a growth role tomorrow**: get great at copywriting — it's the foundation under every other growth activity (ads, organic social, blog posts, tweet threads, landing pages).
- **Paid ads for message-testing**: both speakers agree this rarely works in practice — better to A/B test format/product itself early rather than spend cycles on ad-level title/color/font optimization.
- **Biggest wish for the industry**: stop launching unready products — names Apple's "Apple Intelligence" marketing (pushing a feature as the reason to upgrade before the feature actually ships/works) as the current worst offender; ship it, make sure it performs, *then* market it hard.
- **Biggest mind-change in the last 12 months**: was convinced voice/conversational AI agents would never work well enough (latency too high for natural sub-200ms turn-taking) — reversed after watching ElevenLabs' ~20th customer build a working conversational agent; now personally prefers AI customer support to human agents in many cases (more knowledgeable, can escalate correctly, no social performance of fake politeness required).
- **Why inbound SDR is a dying role**: the actual function of most inbound SDRs is BANT data collection (budget/authority/need/timing) before handoff to an AE — that's a form, not a relationship, and a conversational AI agent can run the same qualification faster with less friction than a multi-step form or a scheduled human call; floated idea — clone the AE's own voice for the qualification bot so it reads as the AE pre-screening their own pipeline.
- **Infrastructure-layer vs. application-layer question**: infrastructure players (ElevenLabs, compare Synthesia, Captions, [[entities/heygen|HeyGen]]) *can* become the application, but only by being explicit about which layers they intentionally stay out of — ElevenLabs' stated boundary: own end-to-end conversational-AI-agent infrastructure, explicitly do not build full digital-avatar platforms, precisely so avatar-platform companies remain trusted partners/customers rather than competitors.
- **Best growth strategy observed in the last 12–18 months**: [[entities/bryan-johnson|Bryan Johnson]]'s "Don't Die" — judged genuinely authentic (not just controversy-for-reach), with three compounding elements: deliberate, sustained controversy (unusual dress, public blood-transfer experiments) that keeps him in conversation; sharply dialed-in, catchy brand messaging ("Don't Die") plus real community; and constant, high-frequency distribution via reactive engagement — jumping into others' viral tweets about all-nighters or junk food in character, in real time.

## Founder Origin Notes (context, not tactical alpha)

- Harries met ElevenLabs co-founder [[entities/mati-staniszewski|Mati Staniszewski]] at a Cambridge hackathon at 19; the same hackathon also connects to Wordware's founder (largest YC raise ever, ~$40M) — Harries' explicit advice: **"do hackathons with your smartest friends."**
- Harries passed on angel-investing in ElevenLabs pre-launch specifically because he thought "build the best model, then figure out who to sell it to" was a bad go-to-market plan — flagged in retrospect as a costly miss, and offered as a caution against pattern-matching go-to-market conventionally when the underlying technology is category-defining.
- Prior venture, Fella (with co-founder Richie): pivoted through COVID drive-through testing (in San Francisco, non-profit; the partner company they distributed for, Autonomy, pivoted into COVID testing and became Curative, one of the fastest companies ever to $100M revenue) into a GLP-1/weight-loss digital clinic reaching ~$300K revenue before flatlining. Harries' own stated lesson: he was too impatient and pushed to pivot B2B; his co-founder wanted to stay the course on the consumer thesis, stayed, and grew the company past $30M/year post-Ozempic wave. **Stated lesson: commit for the long term and be patient — market timing can make an otherwise-correct thesis look wrong if you're early.**

## Notable Quotes

> "Choose your one ICP and build all the products around it to have them compound. However, that's not actually what we're doing."

> "Don't expose your whole product. Don't give it all away for free, but [find] small bits of value... so people can experience that wow moment as quick as possible."

> "If it's positive, that basically means they should be putting their foot on the gas as quickly as possible."

> "I think there is such thing as bad press, particularly if you're trying to sell to enterprises."

## Entities Mentioned

- [[entities/elevenlabs|ElevenLabs]] — the company; $281M raised, $3.3B valuation at time of recording
- [[entities/luke-harries|Luke Harries]] — Head of Growth, ElevenLabs; prior: Post Hoc, Microsoft; angel investor (Lovable, Runna, Captions)
- [[entities/harry-stebbings|Harry Stebbings]] — host, 20VC/20 Growth
- [[entities/mati-staniszewski|Mati Staniszewski]] — ElevenLabs co-founder/CEO
- Superhuman — cited cautionary example, founder-led launch video [not a wiki entity page]
- Ramp / Brex — counter-positioning example [not wiki entity pages]
- TBPN / All-In podcast — counter-positioning example [not wiki entity pages]
- [[entities/lovable|Lovable]] — cited for consumer NRR framing and as an AI app builder already in the wiki
- [[entities/bryan-johnson|Bryan Johnson]] — cited as best recent growth strategy ("Don't Die")

## Concepts Touched

- [[concepts/sharded-growth-teams]] — new
- [[concepts/growth-hiring-order]] — new
- [[concepts/launch-playbook]] — new
- [[concepts/growth-video-strategy]] — new
- [[concepts/seo-mini-tools]] — new; extends [[concepts/ai-search-seo]]
- [[concepts/cac-payback-period]] — new
- [[concepts/product-engineers-no-pms]] — new
- [[concepts/counter-positioning]] — new
- [[concepts/founder-brand-strategy]] — new
- [[concepts/icp-avatar]] — touched (messaging/positioning discipline overlaps)
- [[concepts/gtm-engineering]] — touched (growth-as-merged-function overlaps with the merged PM/marketing thesis)

## My Notes

This source is a genuine domain shift for the wiki: everything ingested previously is B2B cold-email / signal-driven outbound / AI GTM-agent tooling. This episode is general growth marketing — launches, video, brand, org design, retention framing — for a company selling both consumer and enterprise. There's very little literal overlap in tactics with the cold-email stack, but real overlap in *underlying principles*: messaging discipline (→ [[concepts/icp-avatar]]), the merged marketing+product role (→ [[concepts/gtm-engineering]]'s product-engineer thesis), and the general "PMF before paid spend" sequencing which implicitly critiques jumping straight to the paid-ads/UGC-ad playbooks already in this wiki without validating product-market fit first — worth flagging as a soft tension, not a contradiction, since the existing paid-ads sources (Schneider) assume PMF is already established.

## See Also

- [[concepts/icp-avatar]] — messaging discipline parallel
- [[concepts/gtm-engineering]] — merged-function organizational parallel
- [[concepts/ai-search-seo]] — SEO-in-the-AI-era parallel/extension
- [[concepts/growth-loop]] — the launch-then-amplify cycle is a growth loop in miniature
- [[sources/theory-fb-ads-library-claude-saas]] — contrast: this wiki's other "paid-before-PMF" tension point
