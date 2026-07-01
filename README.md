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

## Why These

These are the skills that felt most like judgment exports rather than generic tooling wrappers:

- `voice-dna` captures a specific approach to editing toward a real voice
- `coding-guardrails` captures a practical coding discipline
- `new-project-starter` captures a strong bias toward testing the workflow before building the system
- `codex-frontend-taste` captures a product-minded frontend taste layer
- `codex-marketing-taste` captures a more expressive landing-page taste layer

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

## Publishing Notes

- `voice-dna` intentionally excludes any personal writing samples from the source machine.
- Add your own samples to `skills/voice-dna/references/voice-samples.md` if you want stronger voice matching.
- If this repo is public, keep personal writing, work-specific heuristics, and client material out of `references/`.
- If you want a stronger personal version of `voice-dna`, keep that in a private companion repo or outside version control.

## Choosing What To Export

If you add more skills later, the best ones to publish are usually the ones that encode judgment:

- decision frameworks
- review heuristics
- taste layers
- writing approaches

The least interesting ones to publish are usually thin wrappers around generic tools unless you've made them meaningfully opinionated.

## Future Improvements

Possible next steps for this repo:

- add before/after examples for `voice-dna`
- add screenshots or sample outputs for the frontend taste skills
- split public and private variants where a skill depends on personal or work-specific reference material
