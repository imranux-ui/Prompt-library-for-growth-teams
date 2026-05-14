## WF-04 — Content Refresh + Re-rank System
### Phase: EXECUTE → COMPOUND
### Version: 1.0
#
### TRIGGER: GSC shows a page dropping from top-10 or losing >20% clicks MoM
### OUTPUT:  Refreshed article re-published with improved rankings trajectory
### TIME:    ~2 hours per page refresh (human + AI)
###### ─────────────────────────────────────────────────────────────────────

## Overview

Ranking drops are content decay signals. This workflow diagnoses the cause,
updates the content, and re-publishes with a clear re-indexing action.

---

## Step 1 — Human: Identify Drop Pages
**Source:** GSC → Performance → compare last 28 days vs prior 28 days
**Flag pages where:**
- Average position dropped >5 spots
- Clicks dropped >20% MoM
- Impressions are stable but CTR dropped (title tag issue)
- Impressions dropped (lost coverage entirely — possible index issue)

**Collect for each flagged page:**
- URL, target keyword, current position, previous position
- Top competitor URLs currently outranking

---

## Step 2 — Claude: Diagnose the Drop
**Paste the page URL + keyword + competitor URLs into Claude with this prompt:**

```
[EXECUTE] Diagnose this content ranking drop.

Page: [URL]
Target keyword: [keyword]
Current position: [n] (was [n] last month)
Competitor URLs now outranking: [list]

Analyze what likely caused this drop and what type of refresh is needed.
Check for:
1. Intent drift — has the SERP changed format or intent signal?
2. Freshness — does the content have outdated stats, dates, or references?
3. Competitive gap — what do the outranking pages have that ours lacks?
4. GEO weakness — run a rough GEO checklist and flag gaps
5. Structural issue — is the H1, intro, or meta title weak vs competitors?

Recommend one of:
(a) Minor refresh — update stats, date, add FAQ, tweak H1/meta
(b) Major refresh — rewrite 30-50% of the article with new angle/structure
(c) Replace — create a new page targeting this keyword with a better approach
(d) Redirect — merge with a stronger page and 301 redirect

Justify your recommendation.
```

---

## Step 3 — Claude: Execute the Refresh
**Based on Step 2 recommendation:**

For **minor refresh:**
```
[EXECUTE] Refresh the following article. Make only the changes needed to
recover rankings — do not rewrite sections that are working.

Focus on: [paste Step 2 diagnosis]
Article: [paste full text or URL]
```

For **major refresh:** Use `prompts/build/07-expert-longform-writer.md` with
the original brief updated to reflect the new angle.

**Human review gate:**
- [ ] All [STAT NEEDED] flags resolved with current data?
- [ ] New publish date set (signals freshness to Google)?
- [ ] At least one substantive new section or insight added?
- [ ] GEO score ≥12?

---

## Step 4 — Human: Re-publish + Re-index
1. Publish the updated article with today's date
2. Submit URL to GSC → URL Inspection → Request Indexing
3. Share the updated URL on LinkedIn or X (social signal)
4. Check rankings at Day 7, Day 14, Day 30

---

---
