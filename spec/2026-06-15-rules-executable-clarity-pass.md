# Requirement: Rules Executable Clarity Pass

## Source Request

User approved the next optimization on 2026-06-15:

> ok

This approval refers to polishing `rules/` after `flows/`, `tracks/`, and `modes/` were clarified.

## New Requirement

Polish `rules/` so each rule file becomes an executable decision gate instead of a general advice note.

Priority files for this pass:

- `rules/examples-are-not-requirements.md`
- `rules/reference-adaptation.md`
- `rules/verification.md`

Each edited rule file must use clear conditional language:

- Use When.
- Rule.
- If.
- Then.
- Do.
- Do Not.
- Stop And Ask.
- Output Impact.

## Acceptance Criteria

- Example handling is expressed as concrete if/then behavior.
- Reference adaptation states how to transform references into original rules without copying.
- Verification becomes a QA gate with checks before final handoff.
- Rule files remain compatible with the existing `flows/`, `tracks/`, `modes/`, and `output/` layers.
- No `flows/`, `tracks/`, `modes/`, or `output/` files are changed in this pass.

## Conflict Check

No conflict found.

This requirement refines the existing rule layer and preserves the current skill goal.
