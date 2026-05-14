## WF-07 — Expert Review Quality Gate
### Phase: BUILD → EXECUTE
### Version: 1.0
#
### TRIGGER: Any AI-generated draft before human approval to publish
### OUTPUT:  Reviewed, flagged, and approved draft ready for publish
### TIME:    15–20 min per article
### ────────────────────────────────────────────────────

## Overview

No AI draft publishes without this gate. The goal is not to rewrite
everything — it's to catch what AI gets wrong: facts, voice, and claims
that need a human behind them.

---

## Step 1 — Claude: Self-Assessment
At the end of every draft (Prompt 07), Claude outputs:
- GEO score (out of 16)
- Quality gate flags (Critical / High Priority / Advisory)
- List of [STAT NEEDED] and [DATA NEEDED] flags

Human reviewer reads these first before reading the full draft.

---

## Step 2 — Human: Structured Review
Work through this checklist top to bottom. Don't skim.

**Factual accuracy (Critical):**
- [ ] Every statistic verified against a real source
- [ ] Every [STAT NEEDED] flag resolved or removed
- [ ] No claims that would embarrass the client if wrong

**Search intent (Critical):**
- [ ] Article fully satisfies what the searcher was looking for
- [ ] No section that goes off-topic from the keyword intent

**Brand voice (High Priority):**
- [ ] Sounds like the client, not like generic AI content
- [ ] No words from the CLIENT_VOICE avoid list
- [ ] First sentence is a hook, not a topic announcement
- [ ] No "In this article we will..." or "In conclusion..."

**GEO (High Priority):**
- [ ] GEO score ≥12/16 (if not, send back through Prompt 08)
- [ ] FAQ section present with ≥4 questions
- [ ] TL;DR block present

**Pipeline (High Priority):**
- [ ] CTA present, correct URL, matches conversion goal
- [ ] ≥1 contextual internal link to a conversion-relevant page

**Advisory checks:**
- [ ] Schema type recommended and noted for CMS setup?
- [ ] Featured snippet opportunity flagged?

---

## Step 3 — Human or Claude: Fix Flagged Items
For minor fixes (voice, phrasing, CTA): human edits directly.
For structural fixes (missing FAQ, low GEO score): run the relevant prompt.

**Rule:** If more than 3 Critical or High Priority items fail,
send the draft back through Prompt 07 with the specific issues noted.

---

## Step 4 — Human: Approve and Publish
- [ ] All Critical items passing?
- [ ] At least High Priority items passing or flagged for post-publish fix?
- [ ] Publish date, author, and category set in CMS?
- [ ] Add to WF-06 distribution queue?

---

---
