# Style Fit From Requirements Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Ensure frontend style direction is inferred from product requirements before user design language is applied.

**Architecture:** Add one rule file and connect it from `SKILL.md`. `language/` remains an interpretation support layer, not the primary style router.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Create `rules/style-fit-from-requirements.md`.
- Modify `SKILL.md`.
- Modify `language/README.md`.
- Create the matching requirement file under `spec/`.
- Create this plan file under `plan/`.

## Out Of Scope

- Do not modify `tracks/`, `modes/`, `output/`, `examples/`, `evals/`, or `reference/`.
- Do not create scripts or automated checks.
- Do not delete files.

## Implementation Steps

- [ ] Back up `SKILL.md` and `language/README.md` under `E:\codex_backup`.
- [ ] Create `rules/style-fit-from-requirements.md`.
- [ ] Add style-fit routing to `SKILL.md`.
- [ ] Add hard rules in `SKILL.md` that prevent user design language from overriding product requirements.
- [ ] Update `language/README.md` to state that language interpretation is secondary to requirement-based style fit.
- [ ] Verify keywords and confirm no out-of-scope tracked files changed.

## Verification

- Search for `style-fit-from-requirements.md`, `requirements first`, `language second`, and `product-fit`.
- Run `git status --short` and inspect changed paths.

## Risks

- If the rule is too weak, agents may still map user adjectives directly to visual styles.
- If the rule is too rigid, it may ignore legitimate user preference. The rule should explain conflicts and offer options instead of silently rejecting user language.
