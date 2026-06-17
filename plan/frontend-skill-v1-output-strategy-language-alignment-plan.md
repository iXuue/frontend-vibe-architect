# Output Strategy Language Alignment Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Align output templates with the current requirement -> track -> strategy -> mode -> language -> rules -> output flow.

**Architecture:** This is a Markdown template update. It changes output contracts only; routing remains controlled by `SKILL.md`.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Modify `output/requirement-summary.md`.
- Modify `output/design-options.md`.
- Modify `output/design-brief.md`.
- Modify `output/frontend-execution-plan.md`.
- Create the matching requirement file under `spec/`.
- Create this plan file under `plan/`.

## Out Of Scope

- Do not modify `SKILL.md`.
- Do not modify `README.md`.
- Do not modify any runtime layer other than `output/`.
- Do not create scripts or automated checks.
- Do not delete files.

## Implementation Steps

- [ ] Back up the four output templates under `E:\codex_backup`.
- [ ] Add strategy and language interpretation fields to `output/requirement-summary.md`.
- [ ] Add strategy, product-fit evidence, and language tradeoff fields to `output/design-options.md`.
- [ ] Add confirmed strategy and language interpretation fields to `output/design-brief.md`.
- [ ] Add traceability fields to `output/frontend-execution-plan.md`.
- [ ] Verify required keywords and changed paths.

## Verification

- Search output templates for `Primary strategy`, `Secondary strategy`, `Product-fit evidence`, `User language interpretation`, and `Strategy-language conflicts`.
- Run `git status --short` and inspect changed paths.

## Risks

- Adding too many fields could make outputs harder to use.
- Adding strategy fields without traceability could create empty ritual sections. Each added field should support real design decisions.
