---
title: "Ad Library Market Validation"
type: concept
tags: [market-validation, facebook-ads-library, saas, demand-proof, product-discovery]
created: 2026-06-10
updated: 2026-07-28
sources: [theory-fb-ads-library-claude-saas, codyschneider-ad-library-gap-analysis]
---

# Ad Library Market Validation

The practice of using Facebook Ads Library (or equivalent ad intelligence tools) to identify **proven demand** before building a product. The core logic: if someone is spending money to acquire customers for a product — and has been doing so for 1+ weeks — demand is validated. You don't need customer interviews or a waitlist. The ad spend is the signal.

## The Core Insight

Most SaaS validation approaches are forward-looking: you build something, then try to find customers. Ad Library validation is backward-looking: you find what customers are already paying for, then build a better version.

Ads running for 1+ weeks in premium markets (UK, Germany, US, Australia) mean:
1. **Someone paid to test the offer** — real money is on the table
2. **The offer converts well enough to keep running** — it's not a failed test
3. **The pain is real** — people click because the problem resonates

This makes ad longevity a **proxy for product-market fit** before you've built anything.

## The Method (from [[sources/theory-fb-ads-library-claude-saas]])

1. **Spy phase:** Open Facebook Ads Library, filter active ads in quality markets, log 8–10 digital products with longevity (1+ week). Focus on operational pain for small businesses — the kind of pain that recurs weekly.

2. **Score phase:** Feed the list to Claude. Ask it to score each for **SaaS recurring potential** — the filter that separates one-off purchases from subscription-worthy recurring pain.

3. **Specify phase:** Feed Claude the winning pain points + ad screenshots → generate a complete Lovable-ready prompt (full-stack spec including Supabase backend and frontend layout). Optionally use Higgsfield MCP for visual enrichment.

4. **Build phase:** Paste into [[Lovable]] → 75–80% of app generated in one session → fix rough edges (real Supabase, Stripe, Resend, Vercel) → ship quietly to a small relevant list.

## Why "Recurring SaaS" Is the Key Filter

The method only works if the pain is **recurring**. One-off problems produce one-off purchases; recurring operational pain produces subscriptions. Claude's scoring step filters for this: a PDF solving a problem once is not a SaaS opportunity; a tool that automates a weekly reporting headache is.

## Validated Results

The author built 3 of 6 portfolio products using this method. Combined MRR: £2,950. One product reached £487 MRR (19 customers) within 6 weeks of quiet launch. Low support burden because each product "only does one thing well."

## Relationship to Other Signals

| Signal Type | What It Proves | Used In |
|-------------|---------------|---------|
| FB Ads Library (ad longevity) | Demand exists + someone is paying to find it | This concept |
| LinkedIn engagement signals | Buyer intent at the person level | [[Signal Infrastructure]] |
| Reddit pain point mining | Unmet needs expressed organically | [[AI UGC Ads]] |

Ad Library validation is the **market-level** signal; LinkedIn/Reddit signals are the **person-level** signals. They operate at different layers of the [[SaaS Lifecycle]].

## Limitations

- Works for B2SMB products (small business operational pain) — less clear for enterprise or consumer plays
- The "1+ week" rule is a heuristic, not a hard threshold; campaign budgets vary widely
- Community caveat (from [[sources/codyschneider-paid-ads-playbook]]): for low-ticket SaaS, even proven demand may not yield profitable CAC at scale

## A Second Use of the Same Data Source: Creative Gap-Finding (July 2026)

[[sources/codyschneider-ad-library-gap-analysis]] mines the same raw data source — Facebook Ads Library — for a different purpose. This concept uses ad *longevity* as a proxy for product-market fit, to decide whether to build a product at all. [[concepts/competitor-creative-gap-analysis]] instead uses ad *content* — described at the angle/promise/outcome level by an LLM — to map how an entire category talks about itself, for a product that already exists, in order to find unclaimed positioning. Same source, two non-overlapping extraction targets: longevity (this concept) vs. message content (the other).

## See Also

- [[sources/theory-fb-ads-library-claude-saas]] — the primary source demonstrating this method
- [[entities/lovable]] — the build layer; AI app builder that receives the Claude-generated spec
- [[entities/higgsfield]] — optional MCP connector for visual enrichment in the spec
- [[concepts/saas-lifecycle]] — the lifecycle phases this method compresses (Idea → Validation → Build → Launch)
- [[concepts/signal-infrastructure]] — complementary signal layer (person-level vs. market-level)
- [[concepts/ai-ugc-ads]] — also uses Facebook ad intelligence, from the advertiser side
- [[concepts/competitor-creative-gap-analysis]] — second use of Facebook Ads Library data: creative content, not longevity
- [[sources/codyschneider-paid-ads-playbook]] — running FB ads: what the advertisers the Library surfaces are doing
