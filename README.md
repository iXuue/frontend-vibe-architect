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
├─ SKILL.md      # Entry router and pseudo-code routing table
├─ flows/        # Step-by-step workflow
├─ tracks/       # Product and platform design paths
├─ modes/        # Visual direction modes
├─ rules/        # Decision gates and safety rules
├─ output/       # Stable response templates
├─ examples/     # Calibration examples, not fixed templates
├─ spec/         # Requirement records
└─ plan/         # Implementation plans
```

## Workflow

The intended flow is:

1. Read the user requirement.
2. Produce a requirement summary.
3. Choose a primary track and optional secondary track.
4. Choose relevant visual modes.
5. Apply rules for examples, reference adaptation, animation, verification, and change control.
6. Generate 2-4 design directions when needed.
7. Ask the user to choose or refine a direction when the scope is broad or ambiguous.
8. Produce a design brief.
9. Produce execution-ready frontend design steps when implementation planning is requested.
10. Verify or state what remains unverified.

## Examples

The `examples/` folder is a calibration layer.

It shows how an agent should route typical user requests through the skill. It is not a library of fixed design templates.

Current examples:

- `examples/web-product-ai-tool.md`
- `examples/landing-brand-page.md`
- `examples/informal-visual-example.md`

Use examples to understand expected routing and output shape, not to lock the final design.

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
