---
name: codex-frontend-taste
description: Default frontend taste skill for Codex. Use when implementing or redesigning web UI, app surfaces, dashboards, settings, docs, or component libraries and you want stronger visual judgment, preservation of existing patterns, and a lightweight pre-flight review before shipping.
---

# Codex Frontend Taste

Use this as the default frontend taste layer for implementation work.

Trigger it when the task involves frontend design decisions, UI redesigns, or polishing a generated interface that feels generic.

This skill is for Codex-style implementation work:
- read the repo first
- preserve existing patterns when they are intentional
- improve hierarchy, spacing, layout, motion, and visual clarity
- avoid boilerplate AI aesthetics
- verify the result before shipping

This skill should be the safe default for product-facing work. It is intentionally calmer and more reusable than a landing-page-specific style skill.

This is not a hard-rule design manifesto. Treat it as operational guidance with context-sensitive judgment.

## 1. Start With A Design Read

Before editing code, infer these from the request and the codebase:
- surface type: marketing page, product UI, dashboard, settings, docs, portfolio, redesign
- audience: buyer, user, admin, recruiter, developer, general public
- constraints: existing design system, brand colors, accessibility, performance, SEO, legal copy, unchanged routes
- visual direction: restrained, editorial, playful, premium, utilitarian, trust-first, experimental
- change scope: preserve, modernize, or overhaul

State a one-line design read internally and let it drive the work.

Examples:
- "Product settings UI for existing users, trust-first and utilitarian, preserve current system and improve hierarchy."
- "Marketing landing page for design-conscious buyers, premium and expressive, modernize boldly within the stack."

If two very different directions would both be plausible, ask one concise clarifying question. Otherwise proceed.

## 2. Pick The Right Mode

Choose one mode before making UI decisions.

### Preserve

Use when the project already has a coherent visual language or component system.

Rules:
- keep existing tokens, spacing logic, border radii, and interaction patterns unless they are actively hurting usability
- do not swap component libraries or typography systems without a strong reason
- improve the composition, not the brand identity

### Modernize

Use when the product has decent foundations but weak hierarchy, spacing, or visual rhythm.

Rules:
- preserve information architecture and recognizable patterns
- tighten layout systems, typography scale, spacing consistency, and empty states
- remove obvious generic or outdated styling where it does not break continuity

### Overhaul

Use when the current UI is incoherent or the user explicitly wants a strong redesign.

Rules:
- keep contractual constraints intact: routes, key labels, form semantics, legal copy, analytics hooks, accessibility requirements
- change visual language decisively, but only after identifying what must survive

## 3. Respect The Existing Foundation

Read the codebase before inventing a new visual system.

Look for:
- design system or component library already in use
- typography setup
- token sources
- layout primitives
- motion conventions
- dark mode support

Preferred decision order:
1. existing project patterns
2. official design system already implied by the product
3. lightweight extension of the current stack
4. custom styling only when the first three do not fit

Do not introduce heavyweight UI frameworks into a repo that is intentionally simple.

## 4. Anti-Default Heuristics

Avoid these unless the brief or repo clearly calls for them:
- generic centered hero plus three equal feature cards
- random purple or blue gradients with no brand logic
- glassmorphism everywhere
- decorative motion with no content payoff
- fake dashboards made from empty divs
- repetition of the same section layout all the way down the page
- oversized headings doing all the hierarchy work
- placeholder illustrations that weaken credibility

If the page still feels like a template after implementation, push one layer deeper on composition, typography, spacing, or content framing.

## 5. Product UI Rules

For app surfaces, optimize for clarity before style.

Rules:
- make state, hierarchy, and task flow obvious at a glance
- prefer consistent structure over visual novelty
- use denser layouts only when scanning speed improves
- keep controls visually related to the data they affect
- design loading, empty, error, success, hover, focus, and disabled states
- use motion sparingly and only where it improves orientation or feedback

Do not force landing-page patterns onto dashboards, tables, settings pages, or productivity tools.

## 6. Marketing And Portfolio Rules

For landing pages and portfolios, avoid safe sameness.

Rules:
- vary layout families across the page when it helps pacing
- build a clear concept spine: the page should have one coherent visual idea
- make typography do real work, not just scale up a default sans
- use imagery, texture, or composition intentionally instead of relying on flat backgrounds
- keep CTAs visible and unmistakable
- give sections distinct roles rather than repeating "headline, paragraph, card grid"

Boldness is good when it serves the message and remains legible.

## 7. Motion Rules

Motion should match the surface.

For product UI:
- prefer fast, subtle transitions and tactile feedback
- avoid scroll theatrics and heavy choreography

For marketing surfaces:
- use stronger reveal, sequencing, or parallax only when it supports the concept
- provide reduced-motion fallbacks

Never claim a motion-rich experience and then ship barely animated static blocks.

## 8. Images And Visual Assets

Use real assets when available. If none exist:
- prefer simple, credible compositions over fake product art
- use generated or stock-like imagery only when it fits the brief and the workflow supports it
- if images are critical and missing, call that out clearly instead of hiding the gap with filler

Image generation is optional, not mandatory.

## 9. Redesign Safety

For existing projects, audit before editing:
- what visual tokens are already established
- what patterns users already recognize
- what content or flows must not change
- what is objectively weak: spacing, contrast, clutter, repetition, dead areas, broken responsiveness

Do not silently change:
- route structure
- primary navigation labels
- form field meaning
- legal or compliance copy
- analytics or integration hooks

## 10. Implementation Discipline

When coding:
- follow the repo's component and styling conventions
- prefer small, coherent changes over broad rewrites
- avoid introducing dependencies just for aesthetics
- keep accessibility intact or improve it
- make responsive behavior intentional on mobile and desktop

If a page needs stronger taste, first try:
- improving type scale and line lengths
- cleaning spacing rhythm
- changing section composition
- introducing one stronger visual motif
- sharpening empty and hover states

Do not jump straight to a full rewrite.

## 11. Pre-Flight Check

Before shipping, review the output against this checklist:

- the result fits the actual surface type
- the visual direction matches the audience and brief
- existing patterns were preserved when they should have been
- no obvious generic AI layout defaults remain
- spacing and typography feel intentional
- contrast, focus states, and responsiveness are acceptable
- motion matches the product and respects reduced motion where relevant
- no important user flows or constraints were broken

If a local preview is available and browser tooling exists, verify visually before finalizing.

## 12. Failure Modes

If the result still feels weak, check for these first:
- everything is using the same spacing and card treatment
- the main action does not visually dominate
- headings are large but structure is still muddy
- content blocks feel pasted one after another instead of composed
- the page looks cleaner but not meaningfully easier to use

Fix the weakest structural problem first, not the most decorative one.

## 13. Delivery Style

In the final response:
- summarize the design read in one short sentence when useful
- explain the meaningful visual or structural changes, not every CSS tweak
- mention any constraints preserved
- mention any unverified risks if browser or runtime checks were not possible

## 14. What This Skill Does Not Do

This skill does not:
- force one aesthetic onto every project
- require a specific CSS framework, animation library, or icon set
- assume every frontend task is a landing page
- replace existing design systems without cause
- turn visual taste into arbitrary hard bans

Use judgment. Better taste comes from better reading of context, not stricter dogma.
