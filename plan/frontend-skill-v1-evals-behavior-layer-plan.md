# Evals Behavior Layer Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a Markdown eval layer that checks whether the skill routes common frontend requests correctly.

**Architecture:** The eval layer is documentation-based. It lives in `evals/` and references existing skill layers without changing them.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Create `evals/README.md`.
- Create six eval files under `evals/`.
- Create the matching requirement file under `spec/`.
- Create this plan file under `plan/`.

## Out Of Scope

- Do not modify `SKILL.md`.
- Do not modify `README.md`.
- Do not modify `flows/`, `tracks/`, `modes/`, `rules/`, `output/`, or `examples/`.
- Do not create automation scripts.
- Do not delete or rewrite deprecated `reference/`.

## Implementation Steps

- [ ] Create `evals/README.md` with purpose, usage, and structure rules.
- [ ] Create `evals/web-product-ai-tool.md`.
- [ ] Create `evals/landing-brand-page.md`.
- [ ] Create `evals/mobile-app-direction.md`.
- [ ] Create `evals/vague-visual-reference.md`.
- [ ] Create `evals/conflicting-requirements.md`.
- [ ] Create `evals/implementation-before-design.md`.
- [ ] Verify all eval files share the expected headings.
- [ ] Verify no out-of-scope runtime files changed.

## Verification

- Search `evals/` for the required headings.
- Run `git status --short` and confirm only `evals/`, this plan, and the matching spec are added by this task.

## Risks

- If evals include finished design answers, agents may treat them as templates.
- If evals are too vague, they will not catch routing drift.
- If evals duplicate examples, the layer will not add enough value.
