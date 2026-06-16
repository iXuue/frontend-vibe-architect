# Design Strategy Layer Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a `strategy/` layer that translates product requirements and track choice into design priorities before selecting visual modes or interpreting user design language.

**Architecture:** This is a Markdown strategy layer. It sits conceptually after `tracks/` and before `modes/` and `language/`, but this change does not modify routing files yet.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Create `strategy/README.md`.
- Create seven strategy files.
- Create the matching requirement file under `spec/`.
- Create this plan file under `plan/`.

## Out Of Scope

- Do not modify `SKILL.md`.
- Do not modify `README.md`.
- Do not modify `tracks/`, `modes/`, `rules/`, `output/`, `language/`, `examples/`, `evals/`, or `reference/`.
- Do not create scripts or automated checks.
- Do not delete files.

## Implementation Steps

- [ ] Create `strategy/README.md` with purpose, decision order, and topic list.
- [ ] Create `strategy/efficiency-first.md`.
- [ ] Create `strategy/trust-first.md`.
- [ ] Create `strategy/conversion-first.md`.
- [ ] Create `strategy/exploration-first.md`.
- [ ] Create `strategy/expression-first.md`.
- [ ] Create `strategy/data-insight-first.md`.
- [ ] Create `strategy/immersive-first.md`.
- [ ] Verify all strategy files share the required headings.
- [ ] Verify no out-of-scope files changed.

## Verification

- Search `strategy/` for all required headings.
- Search for phrases that enforce requirement-first strategy choice.
- Run `git status --short` and confirm only `strategy/`, this plan, and the matching spec are added by this task.

## Risks

- If strategy overlaps too much with tracks, it will become redundant.
- If strategy overlaps too much with modes, it will become a style selector instead of a product decision layer.
- If strategy ignores user language, it may miss legitimate preference signals.
