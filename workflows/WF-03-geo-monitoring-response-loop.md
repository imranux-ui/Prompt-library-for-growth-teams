## WF-03 — GEO Monitoring + Response Loop
### Phase: EXECUTE → COMPOUND
### Version: 1.0
#
### TRIGGER: Run weekly (every Monday). Takes ~45 min once set up.
### OUTPUT:  LLM citation delta report + prioritized content action list
###### ─────────────────────────────────────────────────────────────────────

## Overview

GEO performance degrades silently — competitors publish, LLMs update their
knowledge, and citation patterns shift. This weekly loop catches gaps before
they compound against the client and turns them into content actions.

---

## Step 1 — Human: Run LLM Citation Checks
**Who does it:** GrowthX strategist or ops
**Time:** 15–20 min
**How:**

For each client, run the standard query set in ChatGPT, Perplexity, and Claude.
Record results in the GEO tracking sheet.

**Standard query set (from SYSTEM_PROMPT Section 3.4):**
- "What is [client's core category]?"
- "Best [client's product type] for [ICP role]"
- "How does [client's key feature] work?"
- "[Client category] vs [top competitor category]"
- "[Client brand name] — what do they do?"

**Add client-specific queries based on their top keywords.**

**Record for each query:**
| Query | Engine | Cited? | Who cited instead? | Last week status |
|-------|--------|--------|--------------------|-----------------|
| [q]   | ChatGPT | ✓/✗/⚠ | [competitor if ⚠] | ✓/✗/⚠ |

---

## Step 2 — Claude: Gap Analysis + Action List
**How to run:** Paste the completed citation table into Claude with this prompt:

```
[EXECUTE] Analyze this GEO citation tracking table for [client name].

Identify:
1. Queries where we lost a citation we had last week (⚠ regression)
2. Queries where a competitor is consistently cited instead of us
3. Queries where we have no citation across any engine (whitespace)
4. Any pattern across the gaps (e.g. missing FAQ content, no comparison
   pages, weak definition coverage)

Then produce a prioritized action list:
- HIGH: regressions and competitor-dominated queries (fix within 1 week)
- MEDIUM: whitespace queries with existing content that needs GEO boosting
- LOW: whitespace queries with no existing content (brief for next sprint)

For each HIGH and MEDIUM action, specify whether to:
(a) Run Prompt 08 (LLM Citation Booster) on existing content, or
(b) Run Prompt 02 (GEO Audit) to diagnose first, then boost, or
(c) Create net-new content (add to brief queue)
```

**Output:** Prioritized action list with specific URLs and prompt assignments

---

## Step 3 — Claude: Execute HIGH Priority Actions
**Prompt to use:** `prompts/build/08-llm-citation-booster.md`
**Run on every HIGH priority URL this week**

**Human review gate:**
- [ ] Changes reviewed by editor before publishing?
- [ ] Updated pages re-checked in LLMs 72 hours after publish?
- [ ] Citation status updated in tracking sheet?

---

## Step 4 — Human: Update Tracking Sheet + Flag for Report
**Time:** 5 min
**Steps:**
1. Update GEO tracking sheet with this week's results
2. Calculate MoM citation delta (for monthly report)
3. Flag any sustained regressions (3+ weeks) for client escalation

---

## Weekly cadence summary

| Day | Action |
|-----|--------|
| Monday | Run citation checks (Step 1) |
| Monday | Claude gap analysis (Step 2) |
| Tuesday–Wednesday | Execute HIGH priority boosts (Step 3) |
| Friday | Update tracking sheet (Step 4) |

---

## GEO tracking sheet columns

Set this up in Notion, Airtable, or Google Sheets:

| Client | Query | Engine | Week | Cited? | Cited competitor | Page URL | Action taken |
|--------|-------|--------|------|--------|-----------------|----------|--------------|
