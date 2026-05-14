# GrowthX AI Prompt Library & Workflows

> Expert-led, AI-powered organic growth — operationalized in Claude.

This repository contains the prompt library, workflow blueprints, and Claude skill that power GrowthX's content system. Everything here is designed to run inside Claude (claude.ai Projects or the Anthropic API) and produces GrowthX-quality output without re-explaining methodology every time.

---

## What's inside

```
growthx-ai-prompts/
├── skill/
│   └── SYSTEM_PROMPT.md          ← Load this once. Everything else builds on it.
├── prompts/
│   ├── strategy/
│   │   ├── 01-seo-opportunity-brief.md
│   │   ├── 02-geo-audit.md
│   │   ├── 03-serp-competitor-teardown.md
│   │   └── 04-vertical-expansion-planner.md
│   ├── build/
│   │   ├── 05-brand-voice-extractor.md
│   │   ├── 06-programmatic-brief-factory.md
│   │   ├── 07-expert-longform-writer.md
│   │   └── 08-llm-citation-booster.md
│   ├── execute/
│   │   ├── 09-content-to-pipeline-qualifier.md
│   │   ├── 10-internal-linking-map.md
│   │   └── 11-multichannel-distribution.md
│   └── compound/
│       ├── 12-monthly-report-narrator.md
│       └── 13-case-study-pipeline-miner.md
├── workflows/
│   ├── WF-01-client-onboarding-strategy-sprint.md
│   ├── WF-02-programmatic-content-at-scale.md
│   ├── WF-03-geo-monitoring-response-loop.md
│   ├── WF-04-content-refresh-rerank.md
│   ├── WF-05-pipeline-attribution-reporting.md
│   ├── WF-06-multichannel-distribution.md
│   ├── WF-07-expert-review-quality-gate.md
│   └── WF-08-experiment-design-launch.md
├── templates/
│   └── CLIENT_CONTEXT.md          ← Fill this per client before any task
└── examples/
    └── sample-content-brief.md    ← Example of a completed brief output
```

---

## Quick start

### Option A — Claude.ai Projects (recommended for teams)

1. Open [claude.ai](https://claude.ai) → **Projects** → **New Project**
2. Paste the full contents of `skill/SYSTEM_PROMPT.md` into **Project Instructions**
3. Fill in `templates/CLIENT_CONTEXT.md` for your client
4. Paste the client context at the top of your first message in the project
5. Then paste any prompt from the `/prompts` folder and run it

Every conversation in the project inherits the skill automatically.

### Option B — API / workflow tools

```python
import anthropic

with open("skill/SYSTEM_PROMPT.md") as f:
    system_prompt = f.read()

with open("templates/CLIENT_CONTEXT.md") as f:
    client_context = f.read()

with open("prompts/strategy/01-seo-opportunity-brief.md") as f:
    user_prompt = f.read()

client = anthropic.Anthropic()
message = client.messages.create(
    model="claude-sonnet-4-20250514",
    max_tokens=4096,
    system=system_prompt,
    messages=[
        {"role": "user", "content": client_context + "\n\n" + user_prompt}
    ]
)
print(message.content[0].text)
```

---

## How the system is structured

### The Skill (`skill/SYSTEM_PROMPT.md`)
The single source of truth. Load it once as a system prompt. It encodes:
- GrowthX's four-phase methodology (Strategy → Build → Execute → Compound)
- SEO principles: keyword intent labeling, KD targets, E-E-A-T standards, on-page structure
- GEO principles: 6 writing patterns that increase LLM citation probability, scored audit checklist
- Brand voice system: house voice defaults + per-client `CLIENT_VOICE` schema
- 5 standardized output formats (keyword brief, content brief, GEO audit, monthly report, case study)
- 3-tier quality gates (Critical / High Priority / Advisory)
- Operating rules: always-do, never-do, escalation triggers

### Prompts (`/prompts`)
Individual task prompts organized by GrowthX phase. Each file is self-contained and designed to be pasted on top of the loaded skill. They include:
- The task instruction
- Required inputs (what to provide before running)
- Expected output format
- Quality checks specific to that task

### Workflows (`/workflows`)
Multi-step sequences that chain prompts together. Each workflow file documents:
- The trigger (when to use it)
- All steps in order, with the prompt to run at each step
- Human review gates
- Output handoff between steps

### Templates (`/templates`)
Fillable context files. The `CLIENT_CONTEXT.md` is the only thing that changes between clients — fill it in once per engagement and paste it at the start of each session.

---

## The GrowthX Four Phases

| Phase | What it covers | Key prompts |
|-------|---------------|-------------|
| **Strategy** | Keyword mapping, AI visibility audit, competitor analysis | 01, 02, 03, 04 |
| **Build** | Brand voice, content briefs, first drafts, GEO optimization | 05, 06, 07, 08 |
| **Execute** | Pipeline conversion, internal linking, distribution | 09, 10, 11 |
| **Compound** | Monthly reporting, case studies, experiment design | 12, 13 |

---

## GEO scoring quick reference

Every long-form piece should score ≥12/16 on the GEO checklist before publish:

| Check | Points |
|-------|--------|
| Clear standalone definition of core topic | 0–2 |
| Named statistic with source attribution | 0–2 |
| Covers alternatives / competitors | 0–2 |
| FAQ section (≥4 questions) | 0–2 |
| Named framework or proprietary term | 0–2 |
| TL;DR / key takeaways summary block | 0–2 |
| H2/H3 headers mirror common queries | 0–2 |
| Internal links to topical cluster | 0–2 |
| **Target** | **≥12** |

---

## Contributing & versioning

When updating any file in this repo:
1. Bump the version number at the top of the changed file
2. Add a one-line changelog entry under `## Changelog` in that file
3. Test with the three smoke-test prompts in `skill/SYSTEM_PROMPT.md` (Section 9)
4. Open a PR with the client use case that prompted the change

---

## License

Internal GrowthX use. Not for redistribution.
