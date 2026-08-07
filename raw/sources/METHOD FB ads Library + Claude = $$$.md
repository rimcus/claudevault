---
title: "[METHOD] FB ads Library + Claude = $$$"
source: "https://www.blackhatworld.com/seo/method-fb-ads-library-claude.1818434/"
author:
  - "[[Yupwork Elite Member Jr. VIP Jan 2]]"
  - "[[2019 1]]"
  - "[[863 1]]"
  - "[[084]]"
  - "[[V vince.dermi.na Newbie May 21]]"
  - "[[2026 19 6]]"
  - "[[slowslow Regular Member Jr. VIP Mar 2]]"
  - "[[2025 330 70]]"
published: 2026-05-21
created: 2026-06-10
description: "Instead of guessing what might sell, I open the Facebook Ads Library and look for digital products that have been running ads for at least a week in decent..."
tags:
  - "clippings"
---
- The rules for submitting a Dispute have been clarified. Please make certain you [read the rules clarification(s)](https://www.blackhatworld.com/seo/may-2026-dispute-resolution-rules-clarifications.1818087/) OR [read the full DR rules.](https://www.blackhatworld.com/seo/dispute-resolution-rules-procedures.1246633/)

[Jump to new](#post-20792057) [Watch](https://www.blackhatworld.com/seo/method-fb-ads-library-claude.1818434/watch)

#### Theory Of Everything

##### Junior Member

Instead of guessing what might sell, I open the Facebook Ads Library and look for digital products that have been running ads for at least a week in decent countries (UK, Germany, US, Australia).  
  
Filter for active ads, note the ones that feel like they solve a proper operational headache for small businesses. I log the product name, landing page, and ad link in a basic spreadsheet.  
  
After 8–10 examples I drop the list into Claude and ask it to score them for a recurring SaaS version instead of a one-off PDF. Last round it flagged a niche around simple tracking and reporting for small service teams, the kind of thing that shows up in trades and compliance spaces.  
  
I didn’t copy the original product. I fed Claude the pain points and a couple of example screenshots and asked it to write a complete Lovable-ready prompt: full backend logic for Supabase (auth, database tables, check-in flows, basic dashboards), plus a clean frontend layout.  
  
I also hooked Claude up to Higgsfield via the custom MCP connector. It lets the prompts pull in decent images and structured visuals automatically and turns the output from basic text into something that actually looks usable.  
  
Pasted the whole thing into Lovable. Got 75-80% of the app in one go.  
  
Then I spent the next nine days fixing the rough edges myself:  
- Switched straight to a real Supabase project (I don’t touch Lovable Cloud for anything with paying users anymore. it’s just a more expensive wrapper)
- Added Stripe live keys for monthly billing
- Set up Resend for simple notifications
- Hosted on Vercel for front end
Launched quietly to a small relevant list and a couple of groups.  
  
Six weeks later this one product is at £487 MRR with 19 customers. Almost no support work because it only does one thing well.  
  
Portfolio is now £2,950 combined MRR across the six tools. This workflow has been responsible for the last three.  
  
The method is repeatable and dead simple:  
1. Spy on what’s already getting ad spend in the Facebook Ads Library.
2. Use Claude (with the Higgsfield connector if you want richer output) to turn the best pain point into a full Lovable prompt.
3. Build the MVP in Lovable, connect proper Supabase + Stripe.
4. Fix the ugly bits over a few days and ship.
It stops you wasting time on ideas nobody will actually pay for month after month. I still feel like I’m cheating a bit, but the numbers keep working.
