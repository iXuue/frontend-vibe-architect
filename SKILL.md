---
name: frontend-future-design
description: Use when the user wants an agent to read frontend requirements, design product-appropriate UI options, and produce execution-ready frontend design steps for websites, web apps, dashboards, AI tools, mobile directions, mini program directions, desktop software directions, or data visualization surfaces.
---

# Frontend Future Design

This skill reads a user's requirement document, classifies the frontend product surface, proposes design directions, and converts the selected direction into execution-ready frontend design steps.

## Layered Reading Order

1. Read `flows/intake.md`.
2. Read `flows/choose-track.md`.
3. Read the selected file from `tracks/`.
4. Read `rules/reference-adaptation.md`.
5. Read `rules/examples-are-not-requirements.md`.
6. Read the relevant files from `modes/`.
7. Read any relevant files from `rules/`.
8. Use the required template from `output/`.

## Mandatory Sequence

1. Intake the requirement.
2. Output a requirement summary.
3. Choose one primary track and optional secondary track.
4. Choose one or more visual modes.
5. Generate 2-4 design options when direction is not already precise.
6. Ask for user direction when scope is broad, high-impact, or visually ambiguous.
7. Produce a design brief after the direction is confirmed or low-risk recommendation is justified.
8. Produce execution-ready frontend design steps.
9. Verify against `rules/verification.md` before final handoff for implemented UI.

## Hard Rules

- Do not copy reference skills, websites, wording, examples, prompts, or templates directly.
- Do not turn a user-provided visual example into a fixed requirement unless the user explicitly confirms it.
- Do not force Dynamic Future Mode onto dense operational tools where clarity matters more.
- Do not start implementation for broad UI work before requirement summary, track choice, mode choice, and direction choice are clear.
- If a requested code change is not covered by `spec/`, follow `rules/requirement-change-control.md`.
