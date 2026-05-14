## Prompt 06 — Programmatic Brief Factory
### Phase: BUILD
### Version: 1.0
#
### REQUIRES: CLIENT_CONTEXT + a seed keyword pattern + entity list
### OUTPUT:   Batch of content briefs (one per entity) in standard format
#### ─────────────────────────────────────────

## Task

[BUILD] Generate a batch of content briefs for a programmatic content play.

Using the seed keyword pattern and entity list provided, produce one content brief per entity. Each brief must follow the standard content brief format (SYSTEM_PROMPT Section 5.2) and include:

- A unique H1 that isn't just "[keyword] + [entity]" — make it specific and benefit-driven
- A unique meta title (≤60 chars) and meta description (≤155 chars) per entity
- A core outline that's adapted to the entity (not copy-paste structure)
- At least one entity-specific insight, stat, or angle in "Key Points to Hit"
- Internal link recommendations that connect to the cluster pillar

**Important:** Every brief must produce content that is genuinely different from the others. If the only difference is swapping the entity name, the brief is not good enough.

## Inputs

**Seed keyword pattern:**
(e.g. "best [product type] for [entity]" or "[software category] for [industry]")
[paste here]

**Entity list:**
(e.g. list of industries, cities, roles, use cases, or company sizes)
[paste here]

**Pillar page URL this cluster supports:**
[paste here]

**How many briefs to produce this batch (max 20 per run):**
[number]

**Any entities to skip or treat differently:**
[paste here]
