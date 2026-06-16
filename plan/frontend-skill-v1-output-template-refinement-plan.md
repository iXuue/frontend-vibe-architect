# Output Template Refinement Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Refine the active output templates so the skill can produce clearer requirement summaries, design options, design briefs, and frontend execution plans.

**Architecture:** This change only edits Markdown templates in `output/`. It strengthens the output contract while keeping routing, tracks, modes, and rules unchanged.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Modify `output/requirement-summary.md`.
- Modify `output/design-options.md`.
- Modify `output/design-brief.md`.
- Modify `output/frontend-execution-plan.md`.
- Create this plan file.
- Create the matching requirement file.

## Out Of Scope

- Do not modify `SKILL.md`.
- Do not modify `README.md`.
- Do not modify `flows/`, `tracks/`, `modes/`, or `rules/`.
- Do not delete or rewrite deprecated `reference/`.
- Do not add scripts, dependencies, or automation.

## Implementation Steps

- [ ] Back up all four existing output files under `E:\codex_backup`.
- [ ] Rewrite `output/requirement-summary.md` with confirmed/inferred/open/conflict structure.
- [ ] Rewrite `output/design-options.md` with option comparison, tradeoffs, recommendation, and decision gate.
- [ ] Rewrite `output/design-brief.md` with stable design contract fields and non-goals.
- [ ] Rewrite `output/frontend-execution-plan.md` with implementation order and verification structure.
- [ ] Verify all four files retain `Use When`, `Required Shape`, and `Do Not Omit`.
- [ ] Confirm no out-of-scope files were modified by this task.

## Verification

- Search each output file for `Use When`, `Required Shape`, and `Do Not Omit`.
- Search for key terms: `Confirmed`, `Assumptions`, `Open Questions`, `Risks`, `Verification`.
- Run `git status --short` and confirm this task only adds the new spec/plan and modifies the four output files.

## Risks

- Overly long templates could make the skill harder to use.
- Overly generic templates could fail to improve real frontend design decisions.
- This change must preserve clear separation between requirements, design direction, execution steps, and verification.
