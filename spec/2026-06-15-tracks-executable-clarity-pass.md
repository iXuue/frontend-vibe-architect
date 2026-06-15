# Requirement: Tracks Executable Clarity Pass

## Source Request

User requested on 2026-06-15:

> 那现在你先打磨 tracks/

## New Requirement

Polish `tracks/` so each product/platform track is an executable design decision file, not a short note.

Each `tracks/*.md` file must use a consistent structure:

- Use When.
- Primary Goal.
- Design Priorities.
- Layout Defaults.
- Interaction Defaults.
- Visual Risk.
- Do.
- Do Not.
- Output Notes.

The track files must help the agent choose product-appropriate frontend structure before choosing visual style.

## Affected Files

- `tracks/web-product.md`
- `tracks/landing-brand.md`
- `tracks/mobile-direction.md`
- `tracks/desktop-direction.md`
- `tracks/data-visualization.md`

## Acceptance Criteria

- Every `tracks/*.md` file uses the same heading structure.
- Every track states when it should be used.
- Every track states layout and interaction defaults.
- Every track states visual risks and misuse cases.
- Every track includes output notes for design options and execution planning.
- No `flows/`, `modes/`, `rules/`, or `output/` files are changed in this pass.

## Conflict Check

No conflict found.

This requirement refines the existing track layer and does not change the skill's product goal.
