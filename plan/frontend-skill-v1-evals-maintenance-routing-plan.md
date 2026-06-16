# Evals Maintenance Routing Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Connect the existing `evals/` layer to the skill maintenance workflow without making it part of normal runtime routing.

**Architecture:** This is a documentation and routing-boundary update. `SKILL.md` defines agent behavior; `README.md` explains the repository structure.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Modify `SKILL.md`.
- Modify `README.md`.
- Create the matching requirement file under `spec/`.
- Create this plan file under `plan/`.

## Out Of Scope

- Do not modify `flows/`, `tracks/`, `modes/`, `rules/`, `output/`, `examples/`, `evals/`, or `reference/`.
- Do not create scripts or automated test runners.
- Do not delete any files.

## Implementation Steps

- [ ] Back up `SKILL.md` and `README.md` under `E:\codex_backup`.
- [ ] Add `Eval Routing` to `SKILL.md`.
- [ ] Add hard rules in `SKILL.md` that prevent evals from being used as normal design templates.
- [ ] Add `evals/` to the `README.md` layered structure.
- [ ] Add a short `Behavior Evals` section to `README.md`.
- [ ] Verify keywords and confirm no out-of-scope files changed.

## Verification

- Search `SKILL.md` for `Eval Routing`, `evals/`, and `normal frontend design work`.
- Search `README.md` for `Behavior Evals` and `evals/`.
- Run `git status --short` and confirm only the intended files are modified or added.

## Risks

- If `evals/` is described as runtime input, agents may waste context during normal frontend work.
- If `evals/` is not described at all, future skill changes may skip behavior regression checks.
