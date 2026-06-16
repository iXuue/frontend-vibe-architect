# Evals Strategy Routing Requirement

## Background

The main skill route now includes `strategy/` after track selection and before mode or language interpretation.

The eval layer still checks track, mode, rules, and output templates, but it does not yet check expected strategy selection. This means future routing changes could skip `strategy/` without being caught by behavior evals.

## Requirement

- Update eval documentation and eval cases to include expected strategy routing.
- Add `Expected Strategy` to the required eval shape.
- Place `Expected Strategy` after `Expected Track` and before `Expected Modes`.
- Each eval must state whether a final strategy should be selected or whether the agent must stop and ask before strategy selection.

## Scope

- Modify `evals/README.md`.
- Modify six eval case files.
- Create this requirement file.
- Create the matching plan file.

## Out Of Scope

- Do not modify `SKILL.md`.
- Do not modify `README.md`.
- Do not modify `strategy/`, `tracks/`, `modes/`, `rules/`, `output/`, or `language/`.
- Do not add scripts.
- Do not delete files.

## Acceptance Criteria

- `evals/README.md` includes `Expected Strategy` in the required eval shape.
- All six eval case files include `## Expected Strategy`.
- Vague or under-specified requests explicitly prevent final strategy selection until clarification.
- Specific requests include strategy file expectations that match the product requirements.
