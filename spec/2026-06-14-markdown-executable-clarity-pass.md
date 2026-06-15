# Requirement: Markdown Executable Clarity Pass

## Source Request

User approved the next step on 2026-06-14:

> ok

This approval refers to the proposed next step: polish the Markdown skill files so they read like executable agent instructions instead of loose reference notes.

## New Requirement

The first clarity pass must focus only on:

- `flows/`
- `output/`

Each edited Markdown file must use a consistent executable structure:

- Purpose.
- When To Read.
- Inputs.
- Do.
- Do Not.
- Output.
- Stop And Ask.

For output templates, the structure may be adapted into strict response shapes, but the template must still clearly state when to use it, required fields, and what not to omit.

## Acceptance Criteria

- Every `flows/*.md` file has clear responsibility and step boundaries.
- Flow files state what must already be known before the step starts.
- Flow files state what the agent must produce before moving to the next step.
- Output templates are usable as stable response forms, not just loose field lists.
- No track, mode, or rule files are changed in this pass.

## Conflict Check

No conflict found.

This requirement refines the existing layered skill structure and does not change the product goal.
