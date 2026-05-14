# WF-02 — Programmatic Content at Scale
# Phase: BUILD → EXECUTE
# Version: 1.0
#
# TRIGGER: A programmatic keyword play has been approved in the 90-day plan.
# OUTPUT:  Published batch of unique, quality-gated programmatic pages
# TIME:    ~2–3 hours per batch of 10 pages (human + AI combined)
# ─────────────────────────────────────────────────────────────────────

## Overview

Programmatic content scales keyword coverage across entities (industries,
cities, roles, use cases). The risk is generic, copy-paste content that
hurts rankings. This workflow enforces uniqueness at every step.

---

## Step 1 — Human: Define the Programmatic Play
**Who does it:** GrowthX strategist
**Time:** 20 min
**Decide:**
- Seed keyword pattern (e.g. "best [tool] for [industry]")
- Entity list (start with 10–20 entities; expand after results prove out)
- Pillar page this cluster feeds into
- Unique angle per entity — what genuinely differs between entity pages?
  (If nothing genuinely differs, this is not a good programmatic play.)

**Quality bar:** If you can't name one thing that's different about each entity's
page beyond swapping a word, stop and redesign the play.

---

## Step 2 — Claude: Brief Batch
**Prompt to use:** `prompts/build/06-programmatic-brief-factory.md`
**Batch size:** Max 20 briefs per Claude session
**Inputs:** Seed keyword pattern + entity list + pillar URL

**Human review gate — check every brief for:**
- [ ] H1 is unique (not just "[keyword] + [entity]")?
- [ ] "Key Points to Hit" includes at least one entity-specific insight?
- [ ] Internal link to pillar is specified?
- [ ] Outline structure adapted (not copy-paste)?

Reject and regenerate any brief that fails. Do not approve a brief you
wouldn't be proud to show a client.

---

## Step 3 — Claude: Draft Batch
**Prompt to use:** `prompts/build/07-expert-longform-writer.md`
**Run once per approved brief**
**Tip:** Run 3–5 drafts in parallel in separate Claude conversations to save time

**Each draft must include:**
- TL;DR block
- Direct definition of the topic
- Entity-specific stat or insight (flagged as [STAT NEEDED] if Claude can't verify)
- FAQ section (4+ questions)
- CTA matching client's conversion goal
- GEO self-assessment score at the end

**Human review gate — spot check 20% of drafts:**
- [ ] GEO score ≥12/16?
- [ ] Content is genuinely unique (not templated)?
- [ ] No fabricated statistics (all [STAT NEEDED] flags resolved)?
- [ ] Voice matches CLIENT_VOICE?
- [ ] Word count within ±15% of brief target?

---

## Step 4 — Human: Expert Review Pass
**Who does it:** Subject matter expert or senior editor
**Time:** 15–20 min per page
**Check:**
- Factual accuracy (especially any stats or claims)
- Brand voice — does it sound like the client?
- Any claims that need client approval before publishing?
- CTA is correct and link is live

**Rule:** No page publishes without a human having read it top to bottom.

---

## Step 5 — Claude: GEO Optimization Pass
**Prompt to use:** `prompts/build/08-llm-citation-booster.md`
**Run on any draft that scored <12 on GEO self-assessment**
**Input:** Draft text + GEO score + top 2 LLM queries this page should answer

---

## Step 6 — Human: Publish + Internal Linking
**Who does it:** GrowthX ops or client CMS manager
**Steps:**
1. Publish approved pages
2. Run `prompts/execute/10-internal-linking-map.md` with all new URLs added
3. Implement internal link recommendations within 48 hours of publish
4. Add pages to rank tracking in GSC or rank tracker

---

## Batch cadence

| Batch | Entity count | Review hours | Publish timeline |
|-------|-------------|--------------|-----------------|
| Pilot | 5 pages | 2–3 hrs | Week 1 |
| Scale | 10–20 pages | 4–6 hrs | Weeks 2–4 |
| Expand | 20–50 pages | 8–12 hrs | Month 2+ |

Run pilot batch first. Review rankings and traffic at 30 days before scaling.
