## Prompt 12 — Monthly Growth Report Narrator
### Phase: COMPOUND
### Version: 1.0
#
### REQUIRES: CLIENT_CONTEXT + raw data from GA4, GSC, and CRM for the month
### OUTPUT:   Client-ready executive narrative in GrowthX report structure
##### ─────────────────────────────────────────────────────────────────────

## Task

[COMPOUND] Write the monthly growth report narrative for this client.

Using the raw data provided, produce a client-ready narrative following the GrowthX monthly report structure (SYSTEM_PROMPT Section 5.4). This goes into the MBR deck or is sent directly to the client — it must be clear, specific, and connected to business outcomes.

Requirements:
- Lead with the single most impressive number as a headline result
- Every metric must include MoM delta (and YoY if available)
- Rankings section: list specific keywords that moved into #1–3, not just "rankings improved"
- GEO section: report which LLM queries the client is now cited for vs last month
- Pipeline section: connect organic traffic to actual demo requests or leads if data is available
- Next 30 days: 3 specific priorities — not generic ("keep publishing") but named actions ("publish the ABM pillar page, refresh the pricing comparison, run GEO audit on top 5 pages")
- Risks/flags: honest. If a metric dropped, say so and explain why

Tone: confident, data-driven, honest. No spin. No padding. Write as if the client will share this with their board.

## Raw data to narrate

**Date range:** [e.g. April 1–30, 2026]

**Traffic (from GA4 or GSC):**
- Organic sessions: [this month] vs [last month] vs [same month last year]
- Clicks: [this month] vs [last month]
- Impressions: [this month] vs [last month]

**Rankings (from GSC or rank tracker):**
- New #1–3 rankings: [keyword list]
- Notable movers (up): [keyword, position change]
- Notable movers (down): [keyword, position change]

**GEO citations:**
- Queries now cited in ChatGPT: [list]
- Queries now cited in Perplexity: [list]
- Queries now cited in Claude: [list]
- MoM delta: [+/- N citations]

**Pipeline (from CRM or analytics):**
- Demo requests from organic: [number] vs [last month]
- Form fills / trials from organic: [number] vs [last month]
- Revenue attributed (if available): [amount]

**Content published this month:**
- Total pieces: [number]
- Top performer by traffic: [URL] — [sessions]
- Top performer by conversion: [URL] — [conversions]

**Any anomalies, algorithm updates, or issues to flag:**
[paste here]
