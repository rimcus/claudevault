---
title: "Launch Playbook (Tiered)"
type: concept
tags: [launches, growth-marketing, distribution, messaging]
created: 2026-07-15
updated: 2026-07-15
sources: [lukeharries-elevenlabs-growth-playbook]
---

# Launch Playbook (Tiered)

*A three-tier launch classification paired with a fixed, repeatable checklist for turning a shipped product into 200K–700K views.*

## Overview

[[entities/luke-harries|Luke Harries]] (Head of Growth, [[entities/elevenlabs|ElevenLabs]]) runs every product/feature ship through the same checklist, scaled to the launch's tier. The system separates *what deserves attention* (tiering) from *how attention gets executed* (the fixed asset-and-distribution sequence), so the team never re-derives launch strategy from scratch and never over-invests in a minor changelog item.

The mechanism is deliberately front-loaded on messaging, not assets: nobody drafts a video or a tweet until the team has answered "what are we launching, for who, why do they care" and distilled that into one *primary* value proposition repeated everywhere, plus secondary props for depth.

## Key Properties / Characteristics

- Three tiers by impact, not by effort already spent: Tier 1 (major new model or product line) gets the majority of team attention; Tier 2 (feature customers will notice); Tier 3 (changelog entry only).
- Tier 1 launches are owned by the growth lead for that specific product, not by a central marketing function.
- Messaging phase precedes asset creation, always: audience → KPIs → core value props → one consistent primary message, repeated verbatim across every asset and every team member's individual posts.
- Asset build order is fixed: tweet thread first, launch video second, blog post third.
- Distribution is simultaneous and total: every channel, every time, regardless of current audience size there.
- An internal "amplification" step (team-wide resharing within minutes of publishing) is treated as a required distribution step, not an optional nicety.

## How It Works

1. **Define the launch.** For a Tier 1 example (ElevenLabs' speech-to-text launch): decide the primary message ("the most accurate speech-to-text model") and the secondary messages (feature-complete: diarization, character-level timestamps, 99 languages). The primary message is what gets repeated by the growth lead, Harries, and the entire team, every time, in every channel.
2. **Build assets in order.**
   - *Tweet thread first* — it's the fastest to iterate and forces the messaging to be genuinely tight before anything else gets built around it. See tweet-thread mechanics under [[concepts/growth-video-strategy]]'s sibling notes in the source page.
   - *Video second* — for Tier 1, default to motion design (see [[concepts/growth-video-strategy]]).
   - *Blog post third* — technical depth (benchmarks, "secret sauce") for technical audiences, and the SEO/backlink asset for the launch (see [[concepts/seo-mini-tools]]).
3. **Distribute everywhere at once.** X, LinkedIn, Bluesky, Threads, Product Hunt, Reddit, Hacker News — cross-post to all of them even where the audience is thin today; other platforms' users are still worth reaching, and ignored channels are cheaper to own.
4. **Amplify internally.** An internal Slack channel collects every link (tweet thread, LinkedIn post, etc.) the moment they go live; the whole team reshares and comments within minutes. This is the mechanism, not a courtesy — platforms read 30–40 likes in the first 5 minutes as a signal to promote a post further.
5. **Seed your own network manually.** Pull every contact from 5 years of email, every Twitter follower, every LinkedIn connection, and personally message a meaningful slice of them to boost the launch. Framed explicitly as "be shameless" / "do things that don't scale" — validated independently by [[entities/harry-stebbings|Harry Stebbings]], who personally DM'd his first 50,000 Twitter followers while cross-promoting his newsletter.

## Tweet-Thread Mechanics (a sub-recipe inside step 2)

- First word signals the launch type explicitly: "Introducing," "We're excited to..."
- First tweet: one clean line naming exactly what's launching, plus the launch video attached.
- Follow with a space, then a bullet list or short paragraph of secondary value props.
- Never put the link in the first tweet — X actively downranks it. Put the call-to-action + link in the second-to-last tweet, and make sure that tweet is strong on its own, since most feeds algorithmically show only the first tweet plus the last two.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/lukeharries-elevenlabs-growth-playbook]] | ElevenLabs' major launches typically get 200,000–700,000 views following this exact playbook | high (practitioner, specific, repeated across multiple launches) |
| [[sources/lukeharries-elevenlabs-growth-playbook]] | X down-ranks posts with links in the first tweet of a thread (per Elon Musk's own statement) | medium (secondhand claim, not independently verified in this source) |

## Contradictions & Open Questions

- This playbook assumes an existing engaged network and team large enough to amplify (ElevenLabs has ~200 people). The manual-DM-seeding step scales down to solo founders (per Harries' own worked example: "get every person you've emailed in 5 years"), but the internal-amplification step doesn't scale down the same way — open question for a team of 1–3.
- No mention of paid amplification as part of the Tier 1 playbook; distribution here is entirely organic/owned/earned. Contrast with [[concepts/ai-ugc-ads]] and this wiki's paid-ads sources, which assume paid spend as the default lever.

## See Also

- [[concepts/growth-video-strategy]] — the video-asset half of this playbook
- [[concepts/seo-mini-tools]] — the blog-post/SEO half of this playbook
- [[concepts/counter-positioning]] — messaging strategy that can feed the "primary message" step
- [[concepts/growth-loop]] — launches-as-a-cycle is a growth loop applied to distribution
- [[sources/lukeharries-elevenlabs-growth-playbook]] — primary source
