# Prompt 01 — SEO Opportunity Brief Generator
# Phase: STRATEGY
# Version: 1.0
#
# REQUIRES: CLIENT_CONTEXT loaded in this session
# INPUT:    Paste your inputs below the dashes, then send to Claude
# OUTPUT:   Keyword Opportunity Brief (format per SYSTEM_PROMPT Section 5.1)
# ─────────────────────────────────────────────────────────────────────

## Task

[STRATEGY] Generate a keyword opportunity brief for the client above.

Using the CLIENT_CONTEXT provided, produce a prioritized set of keyword clusters we should target in the next 90 days. For each cluster, provide:

1. The primary pillar keyword with SV estimate, KD estimate, intent label [I/C/B/P], and business value score (1–10)
2. 5–8 supporting keywords with the same data points
3. Recommended content type for each (long-form, comparison, programmatic, case study)
4. Top 2–3 competitor domains currently ranking, with a one-line note on their angle or weakness
5. Our differentiation angle — what will make GrowthX content outrank and outperform them

Prioritize clusters in this order:
- Tier 1: [B] Bottom-funnel and [C] Comparison (highest pipeline impact)
- Tier 2: [I] Informational (topical authority and GEO coverage)
- Tier 3: [P] Programmatic (scale plays for later)

Aim for 3–5 clusters total. Flag any cluster where KD exceeds the client's target range.

## Inputs to provide

**What the client does (1–2 sentences):**
[paste here]

**ICP role and pain (if not in CLIENT_CONTEXT):**
[paste here]

**Any seed keywords or topics the client has already mentioned:**
[paste here]

**Any keywords to explicitly avoid (competitor brand terms, irrelevant verticals, etc.):**
[paste here]

## Quality checks Claude will run
- Business value score justified by pipeline proximity (not just traffic)
- KD within range for client's current DA
- Each cluster has a clear differentiation angle, not just "we'll write it better"
- At least one [B] cluster included in every brief
