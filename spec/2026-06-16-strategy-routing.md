# Strategy Routing Requirement

## Background

The repository now includes a `strategy/` layer for requirement-derived design priorities.

`SKILL.md` and `README.md` do not yet route normal frontend design work through this layer. Without this route, agents may jump from track selection directly to modes or language interpretation, skipping the design strategy step.

## Requirement

- Connect `strategy/` to the main skill routing.
- Place strategy selection after track selection and before mode selection or language interpretation.
- Make clear that a request may have one primary strategy and one optional secondary strategy.
- Update the public repository overview so `strategy/` appears in the layered structure and workflow.

## Scope

- Modify `SKILL.md`.
- Modify `README.md`.
- Create this requirement file.
- Create the matching plan file.

## Out Of Scope

- Do not modify files inside `strategy/`.
- Do not modify `tracks/`, `modes/`, `rules/`, `output/`, `language/`, `examples/`, `evals/`, or `reference/`.
- Do not add scripts.
- Do not delete files.

## Acceptance Criteria

- `SKILL.md` Required Workflow includes strategy selection.
- `SKILL.md` includes a `Strategy Routing` section.
- `SKILL.md` Language Routing runs after strategy choice.
- `README.md` includes `strategy/` in layered structure.
- `README.md` workflow includes strategy selection before visual mode selection.
