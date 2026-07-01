---
name: "new-project-starter"
description: "Use when starting a new project, evaluating whether something is worth building, scoping a prototype, or trying to avoid over-investing before the workflow is proven. Helps define the goal, success bar, baseline, riskiest assumptions, cheapest test, timebox, and decision rule before substantial implementation begins."
---

# Just because you can, doesn't mean you should

Use this skill before substantial implementation work when the real question is whether the idea is worth building, not whether it is technically possible.

## Purpose

Turn vague project energy into a small, testable bet.

The default stance is:

- validate the workflow before building the system
- test the riskiest assumption first
- stop early when the return on effort looks weak

## Workflow

Work through these steps in order.

### 1. Goal

State the job to be done in one sentence.

- Focus on the user outcome, not the implementation.
- Prefer verbs like `capture`, `compare`, `summarize`, `schedule`, `publish`, `triage`.

Example:

- `Capture a Craft kanban card faster than opening Craft manually.`

### 2. Success Bar

Define what must be true for the project to feel worth it.

- Make it comparative when possible.
- Prefer user-experience thresholds over technical milestones.
- Avoid vague success bars like `works` or `is polished`.

Examples:

- `Must be meaningfully faster than opening the original app.`
- `Must take less than 10 seconds on phone.`
- `Must feel easy enough that I would actually use it every day.`

### 3. Baseline

Name the boring default.

- What does the user do today without building anything?
- This is the comparison the project must beat.

Examples:

- `Open Craft and add a card manually.`
- `Search Gmail directly.`
- `Copy the text into Notes.`

### 4. Riskiest Assumptions

List the 1-2 assumptions that could make the whole idea not worth doing.

Prioritize:

- workflow friction
- platform constraints
- adoption friction
- setup burden

De-prioritize implementation detail unless it is the actual blocker.

Examples:

- `iPhone voice capture may still be too fiddly even if technically possible.`
- `The user may not trust the automation enough to rely on it.`

### 5. Cheapest Test

Design the lowest-effort test for those assumptions.

Rules:

- prefer ugly manual prototypes
- prefer one-path tests over reusable systems
- do not build architecture first
- do not add deployment, polish, or abstraction before the test

Examples:

- `Mock the mobile flow with a plain form before building auth and deployment.`
- `Try the platform interaction manually before building the backend.`
- `Use a throwaway script instead of a full app.`

### 6. Timebox

Set a short limit for the spike.

Default:

- `30-45 minutes`

If the riskiest assumption is still unresolved at the end of the timebox, pause and reassess instead of continuing to build.

### 7. Decision Rule

Define in advance what each outcome means.

Use this three-way decision:

- `Continue`: the workflow already beats the baseline or is clearly close.
- `Simplify`: the core idea has promise, but the current implementation path is too heavy.
- `Stop`: the workflow is still annoying, slower than the baseline, or too fragile to justify more effort.

## Codex Behavior

When using this skill:

- surface the success bar before proposing architecture
- challenge hidden scope growth early
- name the riskiest assumption explicitly
- suggest the cheapest realistic test, not the most complete solution
- timebox the spike
- after the spike, make an explicit recommendation: `continue`, `simplify`, or `stop`

## Output Template

Use this structure unless the user asks for something else:

```markdown
Goal: ...

Success bar: ...

Baseline: ...

Riskiest assumptions:
- ...
- ...

Cheapest test: ...

Timebox: ...

Decision rule:
- Continue if ...
- Simplify if ...
- Stop if ...
```

## Heuristics

- Technical possibility is not enough.
- A project that works but does not beat the baseline is not done.
- The first build should prove desirability, not durability.
- When the user sounds excited but the platform is hostile, bias toward a smaller experiment.
- If setup cost is a core part of the user experience, count it as product friction, not just build friction.
