# User Design Language Layer Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a `language/` layer that translates vague user design language into concrete frontend design variables and decision guidance.

**Architecture:** This is a Markdown interpretation layer. It supports intake, track selection, mode selection, and output quality, but does not replace those layers.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Create `language/README.md`.
- Create seven language interpretation files.
- Create the matching requirement file under `spec/`.
- Create this plan file under `plan/`.

## Out Of Scope

- Do not modify `SKILL.md`.
- Do not modify `README.md`.
- Do not modify `flows/`, `tracks/`, `modes/`, `rules/`, `output/`, `examples/`, `evals/`, or `reference/`.
- Do not create scripts or automated checks.
- Do not delete any files.

## Implementation Steps

- [ ] Create `language/README.md` with purpose, usage rules, and topic list.
- [ ] Create `language/user-visual-language.md`.
- [ ] Create `language/product-tone-language.md`.
- [ ] Create `language/layout-language.md`.
- [ ] Create `language/motion-language.md`.
- [ ] Create `language/material-language.md`.
- [ ] Create `language/interaction-language.md`.
- [ ] Create `language/ambiguity-patterns.md`.
- [ ] Verify all topic files share the required headings.
- [ ] Verify no out-of-scope files changed.

## Verification

- Search `language/` for required headings.
- Search for guardrail phrases around subjective language and hard requirements.
- Run `git status --short` and confirm only `language/`, this plan, and the matching spec are added by this task.

## Risks

- If the layer becomes a style dictionary, it will be too shallow.
- If the layer treats user adjectives as fixed design rules, it will conflict with the requirement intake rules.
- If the layer is too broad, agents may not know when to use each file.
