# Strategy Routing Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Route frontend design work through the new `strategy/` layer after track selection and before mode or language interpretation.

**Architecture:** `SKILL.md` defines active agent routing. `README.md` documents the repository structure and intended workflow.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Modify `SKILL.md`.
- Modify `README.md`.
- Create the matching requirement file under `spec/`.
- Create this plan file under `plan/`.

## Out Of Scope

- Do not modify `strategy/` files.
- Do not modify `tracks/`, `modes/`, `rules/`, `output/`, `language/`, `examples/`, `evals/`, or `reference/`.
- Do not create scripts or automated checks.
- Do not delete files.

## Implementation Steps

- [ ] Back up `SKILL.md` and `README.md` under `E:\codex_backup`.
- [ ] Update `SKILL.md` Required Workflow to include strategy selection after track selection.
- [ ] Add `Strategy Routing` to `SKILL.md`.
- [ ] Update `Language Routing` in `SKILL.md` so it follows strategy choice.
- [ ] Add `strategy/` to `README.md` layered structure.
- [ ] Update `README.md` workflow to include strategy selection.
- [ ] Verify keywords and confirm no out-of-scope files changed.

## Verification

- Search `SKILL.md` for `Strategy Routing`, `strategy/README.md`, and each strategy file name.
- Search `README.md` for `strategy/` and `design strategy`.
- Run `git status --short` and inspect changed paths.

## Risks

- If strategy routing is too broad, agents may read too many strategy files.
- If strategy routing is too vague, agents may skip the layer during normal design work.
