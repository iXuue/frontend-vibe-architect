# Document Examples And Deprecated Reference Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Make the skill entry documents clearly describe how to use `examples/` and how to avoid the deprecated `reference/` layer.

**Architecture:** This is a documentation consistency update. The active behavior remains routed through `SKILL.md`; `README.md` explains the repository shape for humans and future agents.

**Tech Stack:** Markdown skill files.

---

## Confirmed Scope

- Modify `README.md`.
- Modify `SKILL.md`.
- Do not modify active layer files under `flows/`, `tracks/`, `modes/`, `rules/`, or `output/`.
- Do not delete `reference/`.

## Implementation Steps

- [ ] Back up `README.md` and `SKILL.md` under `E:\codex_backup`.
- [ ] Update `README.md` layered structure to include `reference/` as deprecated historical context.
- [ ] Replace non-ASCII directory tree glyphs in `README.md` with ASCII-safe tree lines.
- [ ] Add a short deprecated reference section to `README.md`.
- [ ] Add example routing guidance to `SKILL.md`.
- [ ] Add hard rules in `SKILL.md` that prevent copying examples or using deprecated `reference/` as the active route.
- [ ] Verify key phrases are present and `git status` shows no deletion.

## Verification

- Search `README.md` and `SKILL.md` for `examples/`, `reference/`, `deprecated`, and `calibration`.
- Run `git status --short` and confirm no deleted paths appear.

## Risks

- If `reference/` is not clearly marked, future agents may read outdated draft notes as active instructions.
- If examples are described too strongly, agents may copy examples instead of adapting them to product requirements.
