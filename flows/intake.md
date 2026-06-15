# Flow: Requirement Intake

## Purpose

Turn the user's requirement document or lightweight request into a structured requirement summary before any design direction is proposed.

## When To Read

Read this first for every substantial frontend design, redesign, planning, or implementation request.

## Inputs

- User-pasted plain text.
- Markdown requirement documents.
- Local `.md` or `.txt` files when the user provides an explicit path.
- Short user messages that can be normalized into a lightweight requirement document.

V1 does not promise automatic parsing of Word documents, PDFs, images, Figma files, or external product docs unless a later requirement explicitly adds that capability.

## Do

Extract:

- Product goal.
- Target users.
- Target platforms.
- Required pages or screens.
- Core workflows.
- Content constraints.
- Visual constraints.
- Technical constraints.
- Accessibility constraints.
- Acceptance criteria.
- Open questions.
- Potential conflicts.

When the user gives informal or example-based visual language, separate:

- Hard requirements.
- Reference examples.
- Visual intent.
- Forbidden directions.
- Agent assumptions.
- Questions that need confirmation.

Translate examples into design variables before generating design directions. Use variables such as hierarchy, density, motion intensity, material depth, contrast, readability, atmosphere, interaction feedback, platform fit, and performance tolerance.

## Do Not

- Do not treat a user-provided visual example as a fixed requirement unless the user explicitly confirms it.
- Do not skip requirement summary for broad, high-impact, or visually ambiguous work.
- Do not infer native platform compliance from a vague platform mention.
- Do not proceed when requirements conflict.

## Output

Produce a requirement summary using `output/requirement-summary.md`.

The summary must clearly separate confirmed requirements from assumptions and examples.

## Stop And Ask

Stop and ask the user when:

- Product goal is unclear.
- Target platform would materially change the design.
- Required screens or core workflows are missing.
- Requirements conflict.
- Acceptance criteria are missing for a high-impact implementation.
- The user appears to want a specific visual example, but has not confirmed whether it is mandatory.
