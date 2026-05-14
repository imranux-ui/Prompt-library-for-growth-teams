## WF-08 — Experiment Design + Launch
### Phase: COMPOUND
### Version: 1.0
#
### TRIGGER: Monthly, after reviewing report. When you want to test a new
#          content angle, format, or programmatic play.
### OUTPUT:  Scoped experiment with hypothesis, content, and success metrics
### TIME:    1–2 hours to design; 30 days to read results
# ─────────────────────────────────────────────────────────────────────

## Overview

Not every content decision is proven. GrowthX runs structured experiments
to test new angles before scaling them. This workflow keeps experiments
small, readable, and actionable.

---

## Step 1 — Human: Identify the Experiment Opportunity
**Good experiment triggers:**
- A keyword cluster that hasn't performed as expected
- A new content format competitors are using
- A GEO pattern that might boost citation in a new topic area
- A programmatic play the team hasn't tried for this client

**Define:**
- Hypothesis: "We believe that [doing X] will result in [outcome Y]
  because [reason Z]."
- Success metric: What number moves and by how much to call it a win?
- Timeline: 30 days minimum before reading results

---

## Step 2 — Claude: Design the Experiment
**Paste your hypothesis into Claude with this prompt:**

```
[COMPOUND] Design a content experiment for [client name].

Hypothesis: [paste]
Success metric: [paste]
Timeline: [paste]

Produce:
1. Experiment scope — exactly what to build (1–3 pieces, specific formats)
2. Control condition — what existing content or baseline are we comparing against?
3. Variables being tested — what is the ONE thing being changed?
4. Content brief(s) for the experiment pieces (use standard brief format)
5. How to read the results — what signals indicate win, lose, or inconclusive?
6. Compound or kill criteria — if it wins, how do we scale it?
   If it loses, what do we learn?
```

---

## Step 3 — Human: Review + Approve Experiment Design
- [ ] Is the hypothesis falsifiable? (Can we actually know if it worked?)
- [ ] Are we only changing ONE variable? (No multi-variable experiments)
- [ ] Is the success metric measurable with our current tracking?
- [ ] Is the scope small enough to read results in 30 days?

---

## Step 4 — Execute
Run the experiment content through the standard workflow:
- Brief → WF-02 (if programmatic) or Prompt 07 (if long-form)
- Publish → WF-06 (distribution)
- Track → add to GSC rank tracker + GEO monitoring (WF-03)

---

## Step 5 — Human: Read Results at Day 30
Pull data. Compare against success metric. Make the call:

| Result | Action |
|--------|--------|
| Win (metric hit) | Scale — add to standard workflow and next 90-day plan |
| Partial win | Iterate — adjust one variable and re-run |
| Inconclusive | Extend to Day 60 or redesign experiment |
| Loss | Document the learning, kill the play, move on |

---

## Experiment log

Keep a running log in Notion or your project tool:

| Client | Hypothesis | Start date | Success metric | Result | Action |
|--------|-----------|------------|----------------|--------|--------|
