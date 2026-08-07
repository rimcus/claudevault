---
title: "Facebook Ads for SaaS 101"
type: source
tags: [facebook-ads, ugc, ai-video, saas, paid-ads, perplexity, reddit, conversion-events]
created: 2026-06-16
updated: 2026-06-16
sources: [codyschneider-fb-ads-ugc-playbook]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2066626814420701466"
source_type: x-post
---

# Facebook Ads for SaaS 101

**Author:** [[Cody Schneider]] (@codyschneider)
**Published:** 2026-06-15
**Context:** Detailed tactical post on Facebook ads for SaaS. More granular than [[sources/codyschneider-paid-ads-playbook]] (which covers both Google and Facebook at a higher level). Adds the full UGC creative production workflow, specific audience targeting, and conversion tracking technical stack. Companion to [[sources/codyschneider-ai-ugc-ads]].

---

## Core Thesis

Facebook ads for SaaS is a test-volume game. Run 10+ ads per week against the broadest viable audience with a click campaign. Let the algorithm find signal. After 7 days, promote winners into a conversion campaign. Repeat weekly. The creative pipeline starts with Reddit pain points in real customer language — not brand copy.

---

## How to Make the Ads: The Creative Pipeline

### Step 1: Pain Point Research via Perplexity + Reddit

Search Perplexity:
> "pain points [x person] has for [y thing] that my [z product] solves reddit"

This triggers Perplexity to scrape Reddit for target customer pain points in their own language.

Then follow up:
> "exact quotes for the pain points reddit"

Perplexity returns relevant verbatim Reddit quotes — the raw material for scripts.

**Why this matters:** Real customer language eliminates the brand-voice problem. UGC ads that use real complaint phrasing outperform polished brand copy because they match what the viewer already thinks. This extends the [[ICP Avatar]] logic (every phrase from exact customer quotes) into the ad creative layer.

### Step 2: Claude Writes the Scripts

Take the Reddit quotes and prompt Claude to write **10 × 30-second UGC ad scripts**.

Each script is grounded in one or more specific pain point quotes. The UGC format: first-person, problem/solution, casual — replicates the feel of an authentic customer testimonial.

### Step 3: Video Generation

Run the scripts through one of:
- **[[HeyGen]]** — AI avatar video generation
- **[[Seedance]]** — AI video generation
- **[[Veo3]]** — Google's AI video generation model

Result: 10+ video ads per week produced without human creators.

---

## How to Run the Ads: Campaign Structure

### Audience Targeting

**Target: Facebook Business Page Admins**

This is a high-signal B2B proxy on Facebook. Business Page Admins are decision-makers operating small-to-medium businesses — the typical SaaS buyer for tools in the productivity, ops, and service categories.

### Week 1: Click Campaign

- Run all 10+ ads against the Business Page Admin audience simultaneously
- Campaign goal: **clicks** (not conversions)
- Duration: **7 days**
- Let the algorithm surface which creatives generate the most engagement

### After 7 Days: Promote Winners

- Take the top-performing creatives from the click campaign
- Move them into a **conversion campaign** with dedicated budget
- Conversion events: **signup** and **payment**

### Technical: Wiring Conversion Events

Track conversion events by:
1. Push a **custom event to the data layer**
2. Listen with **Google Tag Manager**
3. Send that data back to Facebook

This closes the loop — Facebook's algorithm optimizes for the events that matter (sign-ups and payments), not just clicks.

**Community warning (@heyjibi):** When a winner suddenly stops performing, check the pixel/conversion event first before killing the ad. Misfiring conversion events (not creative fatigue) are responsible for half of sudden performance drops.

### Weekly Iteration

- Repeat the full cycle weekly
- Best performers from each cycle inform the next cycle's creative direction (pain angles, formats, hooks)
- This is the [[Growth Loop]] applied to ad creative: measure → remix winners → generate next cycle

**Also from community (@DVRichardson):** Ensure ad and landing page are aligned — the pain point addressed in the ad should be reflected in the landing page H1/P1. (This is the same message-match principle from [[sources/codyschneider-paid-ads-playbook]].)

---

## Relationship to Other Schneider Paid Ads Content

| Element | This Post | [[sources/codyschneider-paid-ads-playbook]] |
|---------|-----------|----------------------------------------------|
| Targeting | Business Page Admins (specific) | All of Facebook (broad) |
| Creative volume | 10+/week | 10/week |
| Click → conversion phasing | Explicit (7-day click first) | Implicit (winners → own campaigns) |
| Research method | Perplexity + Reddit quotes | Not specified |
| Tracking | GTM + data layer detail | Not specified |

These are complementary, not contradictory. The paid ads playbook is the overview; this post is the execution detail.

---

## Entities Mentioned

- [[HeyGen]] — AI avatar video generation
- [[Seedance]] — AI video generation (new in this post)
- [[Veo3]] — Google's AI video generation model (new in this post)
- [[Graphed]] — promoted (implied analytics layer)

## Concepts Touched

- [[AI UGC Ads]] — this post updates the pipeline with Perplexity research, specific targeting, click→conversion phasing, and GTM tracking
- [[ICP Avatar]] — same principle (exact customer quotes) applied to ad creative research
- [[Growth Loop]] — the weekly iterate-from-winners cycle
- [[GTM Agents]] — the Facebook Ads agent now has a full tactical spec across this post and the paid ads playbook

## See Also

- [[concepts/ai-ugc-ads]] — the broader concept; updated with this post's details
- [[sources/codyschneider-ai-ugc-ads]] — the original UGC pipeline (Exa + CLV measurement)
- [[sources/codyschneider-paid-ads-playbook]] — the higher-level paid ads overview (Google + Facebook)
- [[entities/heygen]] — one of three video generation options
- [[entities/seedance]] — new video generation alternative
- [[entities/veo3]] — Google's video generation model
