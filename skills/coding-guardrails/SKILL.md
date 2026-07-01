---
name: "coding-guardrails"
description: "Use when the task involves writing, debugging, fixing, refactoring, or reviewing code in an existing codebase or new project. Apply these guardrails during scoped implementation work to keep changes clear, minimal, and verifiable. Do not trigger for unrelated writing tasks or broad brainstorming without concrete code work."
---

# Coding Guardrails

Behavioral guidelines for day-to-day coding work. Merge these with project-specific instructions and use judgment for trivial tasks.

## Think Before Coding

Do not assume requirements that were not stated or shown by the codebase.

- State key assumptions explicitly when they affect the implementation.
- Surface ambiguity, tradeoffs, and simpler alternatives before coding.
- If something is unclear enough to risk the wrong change, pause and ask.
- Ground decisions in the actual code, config, tests, and surrounding patterns.

## Simplicity First

Write the minimum code that fully solves the requested problem.

- Do not add features, configurability, or abstractions that were not asked for.
- Avoid speculative generalization for single-use code.
- Prefer straightforward control flow over cleverness.
- If the solution feels larger than the problem, simplify it.

## Surgical Changes

Keep edits tightly scoped to the user's request.

- Touch only the files and lines needed for the task.
- Match the existing style and structure of the project unless asked to change it.
- Do not refactor adjacent code just because you noticed it.
- Clean up imports, variables, and code paths made unnecessary by your own changes.
- If you notice unrelated issues, mention them separately instead of folding them into the diff.

## Goal-Driven Execution

Turn the request into verifiable outcomes and work until those outcomes are checked.

- Define what success looks like before making changes.
- When fixing a bug, prefer reproducing it with a test or clear verification step first.
- When adding behavior, add or update tests when the project has a testing pattern for it.
- Verify the result with the smallest reliable check available: tests, build, typecheck, lint, or a focused manual validation.
- Do not declare completion until the change has been checked or any validation gap has been called out clearly.

## Codex Application

- Follow repository instructions first when they conflict with generic preferences.
- When multiple valid paths exist, explain the tradeoff and choose the simplest sound option.
- When requirements are ambiguous, risky, or likely to cause regressions, stop and realign before proceeding.
- Before finishing, confirm the final change still maps directly to the user's request.
