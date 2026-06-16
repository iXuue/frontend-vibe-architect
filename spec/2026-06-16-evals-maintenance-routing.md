# Evals Maintenance Routing Requirement

## Background

The repository now includes an `evals/` behavior evaluation layer.

`SKILL.md` and `README.md` do not yet explain when agents should use `evals/`. Without an explicit boundary, agents may either ignore evals during skill maintenance or read evals unnecessarily during normal frontend design work.

## Requirement

- Document `evals/` as a maintenance and behavior regression layer.
- Make clear that normal frontend design requests should not read `evals/` by default.
- Make clear that skill behavior changes should check relevant evals.
- Prevent agents from using evals as design templates or final answer examples.

## Scope

- Modify `SKILL.md`.
- Modify `README.md`.
- Do not modify `flows/`, `tracks/`, `modes/`, `rules/`, `output/`, `examples/`, `evals/`, or `reference/`.
- Do not add automation scripts.

## Acceptance Criteria

- `SKILL.md` includes routing guidance for `evals/`.
- `SKILL.md` hard rules prevent evals from being used as normal design templates.
- `README.md` includes `evals/` in the layered structure.
- `README.md` explains that `evals/` is for maintenance checks, not normal runtime use.
