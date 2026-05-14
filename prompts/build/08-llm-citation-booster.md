## Prompt 08 — LLM Citation Booster
### Phase: BUILD
### Version: 1.0
#
### REQUIRES: CLIENT_CONTEXT + existing article (URL or text) + GEO audit score
### OUTPUT:   Rewritten or augmented sections that increase LLM citation probability
###### ──────────────────────────────────────────────────────────

## Task

[BUILD] Rewrite and augment the provided article to maximize its probability of being cited by LLMs (ChatGPT, Perplexity, Claude, Gemini).

Do not rewrite sections that are already strong. Focus edits on the highest-leverage changes only. Produce:

1. **Rewritten intro** — Add a direct, quotable definition of the core topic in the first 100 words if missing
2. **TL;DR block** — If not present, write one (3–5 bullets). If present, improve it for scannability and LLM extraction
3. **Strengthened statistics** — Identify weak or vague claims ("many companies", "studies show") and flag them with [STAT NEEDED: suggest what type of data would strengthen this] for human to source
4. **FAQ section** — If absent, write one with 4–6 questions mirroring PAA and common LLM queries. If present, review and improve
5. **Named framework insertion** — If the client has a proprietary methodology or named process relevant to this article, work it in naturally
6. **H2/H3 audit** — Review headers and rewrite any that don't mirror how a user would phrase the query to an LLM
7. **Comparison block** — If the article doesn't address alternatives or "X vs Y" framing, add a concise section

For each change, note: *Why this increases citation probability.*

Output the full revised sections (not the whole article unless <800 words). Flag which sections to leave as-is.

## Article to improve

**GEO score from audit (if run):** [paste score] / 16

**Article (URL or full text):**
[paste here]

**Top 3 LLM queries this article should answer:**
[paste here]
