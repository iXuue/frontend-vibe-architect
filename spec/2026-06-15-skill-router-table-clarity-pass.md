# Requirement: Skill Router Table Clarity Pass

## Source Request

User requested on 2026-06-15:

> 先把 SKILL.md 写成“伪代码式路由表

## New Requirement

Rewrite `SKILL.md` as a clearer pseudo-code style router.

The file must remain Markdown, not executable code.

It must include explicit if/then routing for:

- Requirement intake.
- Track selection.
- Mode selection.
- Rule selection.
- Output template selection.
- Stop conditions.

The router must guide the agent to read the right layer files without making `SKILL.md` a long reference document.

## Affected Files

- `SKILL.md`

## Acceptance Criteria

- `SKILL.md` includes a `Routing Table` section.
- Routing is written in clear if/then style.
- Track routing points to all five track files.
- Mode routing points to both mode files.
- Rule routing points to examples, reference adaptation, animation, verification, and requirement change control.
- Output routing points to all four output templates.
- Stop conditions are explicit.
- No `flows/`, `tracks/`, `modes/`, `rules/`, or `output/` files are changed in this pass.

## Conflict Check

No conflict found.

This requirement refines the entry layer and does not add runtime script routing.
