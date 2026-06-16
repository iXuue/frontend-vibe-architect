# Evals Strategy Routing Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Update behavior evals so they check the new `strategy/` routing step.

**Architecture:** This is an eval documentation update only. It does not change runtime routing or strategy definitions.

**Tech Stack:** Markdown eval files.

---

## Confirmed Scope

- Modify `evals/README.md`.
- Modify six eval case files.
- Create the matching requirement file under `spec/`.
- Create this plan file under `plan/`.

## Out Of Scope

- Do not modify `SKILL.md`, `README.md`, `strategy/`, `tracks/`, `modes/`, `rules/`, `output/`, or `language/`.
- Do not create scripts or automated checks.
- Do not delete files.

## Implementation Steps

- [ ] Back up all seven eval files under `E:\codex_backup`.
- [ ] Add `Expected Strategy` to `evals/README.md` required shape.
- [ ] Add `Expected Strategy` to all six eval case files.
- [ ] Ensure vague or under-specified evals do not select a final strategy prematurely.
- [ ] Verify all eval files have ten standard headings.
- [ ] Verify no out-of-scope files changed.

## Verification

- Count standard headings in each eval case file.
- Search `evals/` for `Expected Strategy`.
- Run `git status --short` and inspect changed paths.

## Risks

- If strategy expectations are too rigid, evals may reject valid secondary strategy choices.
- If strategy expectations are too vague, evals will not catch skipped strategy routing.
