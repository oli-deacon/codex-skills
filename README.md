# Codex Skills

Reusable Codex skills pulled out into a GitHub-friendly structure.

These are the skills from my local setup that felt the most portable, opinionated, and worth reusing across projects.

## Included Skills

### `voice-dna`

Rewrites drafts so they sound more like a real person and less like polished AI sludge.

Use it for:
- rewriting in someone's voice
- de-slopping prose
- tightening emails, docs, posts, or essays without sanding off the edges

Example prompt:

```text
Use $voice-dna to rewrite this draft in my voice without making it sound overpolished.
```

### `coding-guardrails`

Keeps coding work scoped, simple, and verifiable.

Use it for:
- bug fixes
- refactors
- feature work
- code reviews where you want fewer unnecessary edits and clearer validation

Example prompt:

```text
Use $coding-guardrails to keep this change minimal and make sure we verify it properly.
```

### `new-project-starter`

Pushes early project work toward a cheap test instead of premature system-building.

Use it for:
- new project ideas
- prototypes
- workflow experiments
- "should we even build this?" conversations

Example prompt:

```text
Use $new-project-starter to figure out the goal, riskiest assumptions, cheapest test, and stop/continue rule before we build.
```

### `codex-frontend-taste`

Adds a calmer taste layer for frontend implementation work while preserving the repo's existing patterns.

Use it for:
- product UI
- dashboards
- settings pages
- docs or app surfaces that feel generic and need stronger hierarchy

Example prompt:

```text
Use $codex-frontend-taste to improve this UI without breaking the design system or turning it into generic AI slop.
```

### `codex-marketing-taste`

Adds a stronger visual concept and better layout pacing for marketing-style pages.

Use it for:
- landing pages
- launch pages
- homepage redesigns
- portfolios

Example prompt:

```text
Use $codex-marketing-taste to give this landing page a stronger concept, sharper art direction, and less samey section design.
```

## Install

Copy the skill folders into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R skills/* ~/.codex/skills/
```

## Repo Layout

```text
skills/
  voice-dna/
  coding-guardrails/
  new-project-starter/
  codex-frontend-taste/
  codex-marketing-taste/
```

Each skill folder contains:

- `SKILL.md`: the main instructions
- `agents/openai.yaml`: display metadata and default prompt wiring
- `references/`: optional supporting material for the skill
