# Output Template Structure Refinement Requirement

## Background

The skill has four active output templates:

- `output/requirement-summary.md`
- `output/design-options.md`
- `output/design-brief.md`
- `output/frontend-execution-plan.md`

They currently provide basic field lists, but they do not yet strongly separate confirmed requirements, inferred assumptions, unresolved questions, design tradeoffs, implementation readiness, and verification expectations.

## Requirement

- Refine the four output templates so they produce more useful frontend design deliverables.
- Keep the templates readable and agent-friendly.
- Preserve the existing output layer boundaries.
- Do not change `SKILL.md`, `README.md`, `flows/`, `tracks/`, `modes/`, or `rules/` in this change.
- Do not add scripts or automation in this change.

## Template Requirements

### Requirement Summary

- Separate confirmed facts, inferred assumptions, open questions, conflicts, and acceptance criteria.
- Make user examples visible as examples, not hard requirements.
- Include a decision gate that prevents design work when material ambiguity remains.

### Design Options

- Make each option explain its fit, tradeoffs, visual direction, motion direction, implementation difficulty, and risks.
- Require at least two options for broad, high-impact, or visually ambiguous work.
- Include a recommendation section that states why one option is preferred and what the user must choose.

### Design Brief

- Convert a chosen option into stable design direction.
- Include page/screen structure, component language, visual tokens, motion boundaries, responsive behavior, accessibility notes, and non-goals.
- Prevent untraceable visual decisions.

### Frontend Execution Plan

- Convert the design brief into implementation-ready frontend steps.
- Include build order, component breakdown, state handling, responsive rules, motion rules, asset guidance, and verification steps.
- Require verification to distinguish checked items from unverified claims.

## Acceptance Criteria

- Each output template has clear `Use When`, `Required Shape`, and `Do Not Omit` sections.
- The templates guide an agent toward product-specific design rather than generic visual decoration.
- The templates can be used without reading deprecated `reference/`.
- No files outside `output/`, `spec/`, and `plan/` are modified by this change.
