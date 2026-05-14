# WF-05 — Pipeline Attribution Reporting
# Phase: COMPOUND
# Version: 1.0
#
# TRIGGER: Monthly, before client MBR or growth review
# OUTPUT:  Executive narrative + pipeline attribution summary for MBR deck
# TIME:    ~1.5 hours (human data pull + Claude narrative)
# ─────────────────────────────────────────────────────────────────────

## Step 1 — Human: Pull the Data
**Sources:** GA4, GSC, CRM (HubSpot, Salesforce, Pipedrive)

**Pull these numbers:**
- Organic sessions (MoM, YoY)
- Organic clicks and impressions (GSC)
- Top 10 pages by organic sessions this month
- Top 10 pages by organic-sourced conversions (form fills, demo bookings)
- New #1–3 keyword rankings gained this month
- Deals or pipeline created with organic as first touch or last touch
- GEO citations delta (from WF-03 tracking sheet)

**Format as a simple data table or bullet list — don't write the narrative yourself.**

---

## Step 2 — Claude: Write the Report Narrative
**Prompt to use:** `prompts/compound/12-monthly-report-narrator.md`
**Paste all data from Step 1 as inputs**

**Human review gate:**
- [ ] Headline result is the most impressive defensible number?
- [ ] All MoM deltas correct (double-check the math)?
- [ ] No spin — drops are acknowledged, not buried?
- [ ] Next 30 days priorities are specific actions, not vague goals?
- [ ] Approved by GrowthX lead before sending to client?

---

## Step 3 — Human: Build MBR Deck
1. Drop narrative into slide deck template
2. Add charts from GA4/GSC (screenshots or embedded)
3. Add GEO citation table (from WF-03 tracking sheet)
4. Send to client 24 hours before the MBR call

---

---
