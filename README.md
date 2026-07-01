# Codex Skills

Reusable Codex skills pulled out into a GitHub-friendly structure.

## Included Skills

- `voice-dna`
- `coding-guardrails`
- `new-project-starter`
- `codex-frontend-taste`
- `codex-marketing-taste`

## Why These

These are the most portable and opinionated skills from the local set:

- `voice-dna`: helps rewrite prose toward a real human voice instead of polished AI mush
- `coding-guardrails`: keeps code changes small, grounded, and verified
- `new-project-starter`: prevents overbuilding by forcing a cheap test first
- `codex-frontend-taste`: improves product UI work without flattening everything into generic patterns
- `codex-marketing-taste`: gives marketing and landing-page work a stronger concept and better pacing

## Install

Copy the skill folders into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R skills/* ~/.codex/skills/
```

## Publishing Notes

- `voice-dna` intentionally excludes any personal writing samples from the source machine.
- Add your own samples to `skills/voice-dna/references/voice-samples.md` if you want stronger voice matching.
- If you want a public repo, keep personal examples, company-specific heuristics, and private client material out of `references/`.
- If you want to keep personal voice data in version control, use a private repo or a private companion repo.

## Suggested Repo Shape

```text
skills/
  voice-dna/
  coding-guardrails/
  new-project-starter/
  codex-frontend-taste/
  codex-marketing-taste/
```

## Optional Next Step

If you want to add more skills later, prefer exporting the ones that encode your judgment rather than generic tooling wrappers.
