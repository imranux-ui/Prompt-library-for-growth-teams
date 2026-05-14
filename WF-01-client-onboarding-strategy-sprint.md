# WF-01 — Client Onboarding → Strategy Sprint
# Phase: STRATEGY
# Version: 1.0
#
# TRIGGER: New client signed. Use in the first 2 weeks of an engagement.
# OUTPUT:  90-day content plan + keyword map + AI visibility baseline
# TIME:    ~3–4 hours total (human + AI combined)
# ─────────────────────────────────────────────────────────────────────

## Overview

This workflow takes a new client from zero context to a fully scoped 90-day
organic growth plan. It runs in 5 steps. Steps 1 and 3 require human input.
Steps 2, 4, and 5 are Claude-assisted.

---

## Step 1 — Human: Fill CLIENT_CONTEXT
**Who does it:** GrowthX strategist
**Time:** 30–45 min
**How:**
1. Conduct intake call with client (use intake questions below)
2. Fill in `templates/CLIENT_CONTEXT.md` completely
3. Run brand voice extractor (Prompt 05) against client's existing content
4. Add the resulting CLIENT_VOICE block to CLIENT_CONTEXT

**Intake call questions:**
- What does your product do and who buys it? (product + ICP)
- What does a converted customer look like? (conversion goal)
- What content have you already tried? What worked, what didn't?
- Who are your top 3–5 competitors? Any you admire for content?
- What topics do you want to own in 12 months?
- What's your current monthly organic traffic baseline?
- Do you have existing content? Can you share your top 5 pages?
- What's the one question your buyers ask before they buy?

---

## Step 2 — Claude: SEO Opportunity Brief
**Prompt to use:** `prompts/strategy/01-seo-opportunity-brief.md`
**Inputs:** Completed CLIENT_CONTEXT + intake notes
**Output:** 3–5 keyword clusters, prioritized by pipeline impact

**Human review gate:**
- [ ] Clusters make sense for the ICP? (remove any that don't map to buyer journey)
- [ ] KD targets realistic for current DA?
- [ ] At least one [B] bottom-funnel cluster included?
- [ ] Client approves the topic direction?

---

## Step 3 — Human: Gather Competitor URLs
**Who does it:** GrowthX strategist
**Time:** 20–30 min
**How:**
- For each approved cluster, find the top 3 ranking competitor URLs
- Note any that rank in AI results (ask ChatGPT/Perplexity the core queries)
- Paste URLs into the next step

---

## Step 4 — Claude: Competitor Teardowns + GEO Baseline
**Prompts to use:**
- `prompts/strategy/03-serp-competitor-teardown.md` (run once per top cluster)
- `prompts/strategy/02-geo-audit.md` (run against client's top 3 existing pages if any)

**Output:**
- Differentiation angles per cluster
- GEO scores for existing client content
- List of LLM queries the client is currently NOT cited for

**Human review gate:**
- [ ] Differentiation angles are specific, not generic?
- [ ] GEO baseline documented in client folder?
- [ ] LLM citation gaps noted as priority content opportunities?

---

## Step 5 — Claude: 90-Day Content Plan
**How to run:**
Paste all outputs from Steps 2–4 into a single Claude message with this instruction:

```
Using the keyword clusters, competitor teardowns, and GEO baseline above,
produce a 90-day content plan for [client name].

Structure it as:
- Month 1 (Weeks 1–4): Foundation — pillar pages and top [B] content
- Month 2 (Weeks 5–8): Expand — supporting cluster pages and [C] comparisons
- Month 3 (Weeks 9–12): Scale — programmatic plays and GEO optimization pass

For each piece include: title, target keyword, intent label, content type,
word count target, priority (High/Med/Low), and which GrowthX phase it serves.

Output as a table.
```

**Human review gate:**
- [ ] Plan reviewed with client and approved?
- [ ] Briefs for Month 1 pieces created (use Prompt 06 or 07)?
- [ ] 90-day plan added to project management tool?

---

## Deliverables checklist at end of onboarding sprint

- [ ] CLIENT_CONTEXT.md filled and saved to client folder
- [ ] 3–5 keyword clusters approved
- [ ] GEO baseline score documented
- [ ] 90-day content plan approved by client
- [ ] Month 1 briefs created and in queue
- [ ] Reporting baseline captured (traffic, rankings, LLM citations)
