## Prompt 10 — Internal Linking Map Builder
### Phase: EXECUTE
### Version: 1.0
#
### REQUIRES: CLIENT_CONTEXT + list of published URLs with their target keywords
### OUTPUT:   Internal linking recommendations with anchor text, organized by cluster
# ────────────────────────────────────────────────

## Task

[EXECUTE] Build an internal linking map for the content cluster provided.

Using the URL list and their associated keywords, produce an internal linking plan that:

1. **Identifies the pillar page** for each cluster — or flags if one is missing and recommends creating it
2. **Maps supporting pages to their pillar** — every supporting page should link to the pillar with a keyword-rich anchor
3. **Cross-links supporting pages** where topically relevant — not every page to every page; only where it aids the reader's journey
4. **Recommends anchor text** for every link — specific, descriptive, keyword-relevant (never "click here" or "read more")
5. **Flags orphan pages** — published pages with no inbound internal links
6. **Prioritizes link insertions** — which pages most urgently need links added, and from where

Format output as a table per cluster:

| Source page (URL) | Link destination (URL) | Recommended anchor text | Priority |
|---|---|---|---|

Then add a separate **Orphan Pages** list and a **Missing Pillar** flag if applicable.

## Inputs

**URL list with target keywords (paste as a list or table):**

| URL | Target keyword |
|-----|---------------|
| [url] | [keyword] |
| [url] | [keyword] |

**How many clusters does this site have (approximate)?**
[number]

**Any pages that should NOT be linked to (noindex, thin, deprecated)?**
[paste here]
