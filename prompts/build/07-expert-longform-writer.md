## Prompt 07 — Expert Long-Form Article Writer
### Phase: BUILD
### Version: 1.0
#
### REQUIRES: CLIENT_CONTEXT + a completed content brief (from Prompt 06 or similar)
# OUTPUT:   Full draft article with all GEO patterns applied
#### ──────────────────────────────────────────────────────────────

## Task

[BUILD] Write a full long-form article based on the brief below.

Follow the brief's H1, outline, word count target, and CTA. Apply all GEO writing patterns from the system prompt (definition opener, named data points, comparison framing, FAQ block, named framework where possible, TL;DR summary). Write in the loaded CLIENT_VOICE — if no voice is loaded, use GrowthX house voice.

Article structure requirements:
- **TL;DR block** at the top (3–5 bullets summarizing key takeaways)
- **Hook intro** — answer the core query within the first 100 words; do not announce the article's topic
- **H2 and H3 structure** per the brief outline — adapt if a better angle emerges mid-draft, but flag the change
- **Direct definition** of the primary topic within the first 300 words
- **≥1 named statistic with source** in the body (use "[Source]" placeholder if no data is available — flag for human to verify)
- **≥1 expert POV or practitioner insight** (can be GrowthX voice, client voice, or "[Expert name] recommends..." structure)
- **Comparison section or table** if the topic involves alternatives
- **FAQ section** at the end — minimum 4 questions, 40–80 word answers each, questions should mirror People Also Ask phrasing
- **CTA** matching the client's conversion goal

After the article, output:
- GEO score self-assessment (run the checklist; flag any items below 2)
- 2–3 internal link recommendations with anchor text
- Suggested schema type (Article / FAQ / HowTo)
- Any quality flags triggered

## Content brief to use

[Paste the full content brief here — from Prompt 06 output or manually created]
