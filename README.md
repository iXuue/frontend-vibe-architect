# frontend-vibe-architect

A requirement-driven frontend design skill for turning product needs into structured UI directions and execution-ready frontend design steps.

This skill is designed for agents that need to read a user requirement document, separate real requirements from reference examples, choose the right frontend surface, propose product-appropriate design directions, and prepare implementation guidance.

## What It Does

- Reads frontend requirement documents or lightweight user requests.
- Separates hard requirements, reference examples, visual intent, assumptions, and open questions.
- Chooses the right frontend track, such as web product, landing page, mobile direction, desktop direction, or data visualization.
- Chooses suitable visual modes, such as dynamic future or simple designed.
- Produces multiple design directions before implementation when the request is broad or visually ambiguous.
- Converts a chosen direction into execution-ready frontend design steps.
- Adds verification expectations for implemented UI.

## When To Use

Use this skill when the user wants to design, plan, critique, or implement frontend interfaces such as:

- Websites and landing pages.
- SaaS products and web apps.
- Dashboards and admin panels.
- AI tools and creative tools.
- Mobile app or mini program directions.
- Desktop software directions.
- Data visualization and monitoring surfaces.

## What It Does Not Do

- It does not treat user-provided examples as hard requirements unless explicitly confirmed.
- It does not copy named products, websites, design systems, prompts, or templates directly.
- It does not promise full native iOS, Android, mini program, Windows, or macOS platform compliance in V1.
- It does not automatically parse Word documents, PDFs, screenshots, Figma files, or external product docs in V1.
- It does not replace implementation verification; rendered UI still needs browser or visual QA when code is produced.

## Layered Structure

```text
frontend-vibe-architect
- SKILL.md      # Entry router and pseudo-code routing table
- flows/        # Step-by-step workflow
- tracks/       # Product and platform design paths
- strategy/     # Requirement-derived design priorities
- modes/        # Visual direction modes
- rules/        # Decision gates and safety rules
- output/       # Stable response templates
- examples/     # Calibration examples, not fixed templates
- evals/        # Behavior checks for skill maintenance
- reference/    # Deprecated early draft layer, retained for historical context
- spec/         # Requirement records
- plan/         # Implementation plans
```

## Workflow

The intended flow is:

1. Read the user requirement.
2. Produce a requirement summary.
3. Choose a primary track and optional secondary track.
4. Choose a primary design strategy and optional secondary strategy.
5. Choose relevant visual modes.
6. Apply rules for examples, reference adaptation, animation, verification, language interpretation, and change control.
7. Generate 2-4 design directions when needed.
8. Ask the user to choose or refine a direction when the scope is broad or ambiguous.
9. Produce a design brief.
10. Produce execution-ready frontend design steps when implementation planning is requested.
11. Verify or state what remains unverified.

## Examples

The `examples/` folder is a calibration layer.

It shows how an agent should route typical user requests through the skill. It is not a library of fixed design templates.

Current examples:

- `examples/web-product-ai-tool.md`
- `examples/landing-brand-page.md`
- `examples/informal-visual-example.md`

Use examples to understand expected routing and output shape, not to lock the final design.

## Behavior Evals

The `evals/` folder is a maintenance layer.

Use it when changing this skill's routing, flows, tracks, modes, rules, outputs, examples, or maintenance documentation. It helps check whether a change breaks expected routing, stop conditions, output template use, or forbidden behavior.

Do not read `evals/` by default during normal frontend design work. Do not use eval files as design templates or final answer examples.

## Deprecated Reference Layer

The `reference/` folder is an early draft layer.

It is not the active route for this skill. Future agents should start from `SKILL.md` and the active folders:

- `flows/`
- `tracks/`
- `modes/`
- `rules/`
- `output/`
- `examples/`

Keep `reference/` only as historical context unless a task explicitly asks to inspect old drafts. Do not delete it without separate explicit confirmation.

## Current Status

This is a Markdown-based V1 skill.

The core layers are in place:

- Entry routing.
- Requirement intake.
- Track selection.
- Mode selection.
- Rule gates.
- Output templates.
- Calibration examples.

Future versions may add scripts for consistency checks, routing assistance, or output validation after the Markdown behavior is stable.
