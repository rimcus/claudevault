---
title: "Post by @codyschneider on X"
source: "https://x.com/codyschneider/status/2085395478154281432"
author:
  - "[[@codyschneider]]"
published: 2026-08-06
created: 2026-08-07
description: "half of winning with AI search is just writing content AI wants to consume how to find this with prompt watch api and data for seo api and"
tags:
  - "clippings"
---
half of winning with AI search is just writing content AI wants to consume

how to find this with prompt watch api and data for seo api and write and publish it to your CMS with a coding agent

here's the exact loop i run

1\. find the prompts you're losing

promptwatch api gives you every tracked prompt for your brand plus who got cited in the answer, per model — chatgpt, claude, gemini, perplexity, grok

it also has agent analytics so you can see which AI crawlers actually hit your pages.

pull two lists. prompts where you show up. prompts where a competitor shows up and you don't

list two is your content calendar

2\. size them with dataforseo's ai optimization api

/v3/ai\_optimization/ai\_keyword\_data/keywords\_search\_volume/live — search volume for how people phrase things inside AI tools, not google. totally different phrasing, way longer, way more conversational

/v3/ai\_optimization/llm\_mentions/live — mention counts and impressions for your brand vs competitors on any keyword.

then /v3/ai\_optimization/chat\_gpt/llm\_responses/live and the claude, gemini, and perplexity versions of the same endpoint. same prompt, four models, live. you get the full answer text and every citation

pennies per call no $500/month seat

3\. read the citations before you write a single word

take the top 20 cited URLs across those prompts, have codex code fetch all of them, and tell you what they have in common

it's never "better writing." it's shape:

answer in the first 40 words, before any setup

H2s written as the literal question someone typed

a comparison table with named competitors in it

specific numbers and dates in the same sentence as the claim

200-400 word sections that stand alone

brand name sitting next to the category term over and over

models retrieve chunks, not pages. a 3,000 word essay with the answer buried

in paragraph 14 never gets cited. a page where every section independently answers a question gets cited five different ways

4\. write it with a coding agent, not a chat window

hey claude code, build this:

read prompts.json. for each prompt, fetch every cited URL, extract the heading structure and how the first paragraph answers the question. then write a post

that answers the prompt in the first 40 words, uses the competitors' H2 questions as the outline, includes a comparison table with us in it, and adds FAQ Page + Article schema. output JSON matching my CMS schema.

the reason it has to be an agent: one run hits 4 APIs, fetches 20 pages, and

writes 30 files. you are not copy pasting that out of a chat window

5\. publish over the CMS API

every CMS has one

strapi /api/articles, wordpress /wp-json/wp/v2/posts, ghost /admin/api/posts, webflow (ew)

give the agent the token, have it POST the batch, then hit indexnow and submit to search console

push 20-30 posts in one command. never open the CMS admin

6\. re-run it in two weeks

same llm\_responses calls, same prompts. you're not checking rankings. you're checking whether your URL is in the citations array now

most people are going to spend this year buying an AI visibility dashboard and never change a single page

the dashboard isn't the work

rewriting your content into the shape models actually retrieve is the work

If you want to do this exact system everything you need on graphed .com

---

Graphed .com - Deploy AI Agents for Marketing

Deploy agents that run paid ads, cold outbound, and SEO with the Graphed CLI

Data pipeline, data warehouse and cloud server to host your agents

Grow your business with virtual employees

Learn more at link

[graphed.com Graphed - Deploy AI Agents for Marketing](https://t.co/mL5ZLkAgFP)