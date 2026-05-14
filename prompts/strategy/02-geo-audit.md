# Prompt 02 — GEO (Generative Engine Optimization) Audit
# Phase: STRATEGY
# Version: 1.0
#
# REQUIRES: CLIENT_CONTEXT loaded + a URL or article text to audit
# INPUT:    Paste the URL or full article text below the dashes
# OUTPUT:   Scored GEO Audit Report (format per SYSTEM_PROMPT Section 5.3)
# ─────────────────────────────────────────────────────────────────────

## Task

[STRATEGY] Run a GEO audit on the content provided below.

Score the content against the 8-point GEO checklist (0–2 per item, max 16). Then:

1. Report the total GEO score and status (STRONG ≥12 / NEEDS WORK 8–11 / CRITICAL <8)
2. For each checklist item, give the score AND a one-sentence explanation of why
3. List the top 3 highest-impact actions to improve the score, ordered by effort-to-impact ratio
4. Identify which LLM query types this content is currently positioned to answer — and which it is not
5. Recommend one new section or block to add that would have the biggest GEO impact

If a URL is provided: analyze based on what you know about effective GEO content structure and flag that live page data (real-time rankings, actual LLM citation status) must be verified by the human operator.

If article text is pasted: analyze the full text directly.

## Content to audit

**URL or article text:**
[paste here]

**Primary keyword this content targets:**
[paste here]

**Top 2–3 LLM queries this page should be cited for:**
[paste here]

## GEO Checklist (Claude scores each 0–2)
- [ ] Has a clear, standalone definition of the core topic
- [ ] Contains ≥1 named statistic with source attribution
- [ ] Covers alternatives or competitors
- [ ] Includes an FAQ section (≥4 questions)
- [ ] Uses a named framework, model, or proprietary term
- [ ] Has a TL;DR or key takeaways summary block
- [ ] H2/H3 headers mirror common LLM and PAA queries
- [ ] Internal links to related topical authority content
