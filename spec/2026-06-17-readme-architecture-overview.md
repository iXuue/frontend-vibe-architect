# README Architecture Overview Requirement

## Background

The skill now includes active layers for flows, tracks, strategy, modes, language interpretation, rules, output templates, examples, and evals.

`README.md` lists the structure but does not yet explain the architecture clearly enough for a new reader to understand how these layers work together.

## Requirement

- Improve `README.md` so it explains the current skill architecture and layer responsibilities.
- Show the intended design decision flow from requirement intake to output and evals.
- Make clear that `strategy/` sits after `tracks/` and before `modes/` and `language/`.
- Make clear that `language/` interprets user wording after requirement and strategy analysis.
- Make clear that `evals/` is for maintenance checks, not normal runtime use.

## Scope

- Modify `README.md`.
- Create this requirement file.
- Create the matching plan file.

## Out Of Scope

- Do not modify `SKILL.md`.
- Do not modify `flows/`, `tracks/`, `strategy/`, `modes/`, `language/`, `rules/`, `output/`, `examples/`, `evals/`, or `reference/`.
- Do not add scripts.
- Do not delete files.

## Acceptance Criteria

- `README.md` includes a clear architecture flow.
- `README.md` includes layer responsibilities.
- `README.md` current status reflects strategy, language, and eval layers.
- No runtime layer files are modified.
