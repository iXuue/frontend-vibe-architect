# Flow: Design Options

## Purpose

Generate several product-appropriate design directions before implementation or detailed execution planning.

## When To Read

Read after requirement intake, track choice, and initial visual mode choice.

## Inputs

- Requirement summary.
- Primary and secondary tracks.
- Relevant mode files from `modes/`.
- Relevant rules from `rules/`.
- Any confirmed visual constraints or forbidden directions.

## Do

Generate 2-4 options when the user has not already chosen a precise direction.

Each option must include:

- Name.
- Best-fit scenario.
- Not good for.
- Track.
- Visual mode.
- Visual language.
- Layout strategy.
- Color and material strategy.
- Motion strategy.
- Reference-image direction.
- Implementation difficulty.
- Risks.
- Why this fits the requirement.

Include both Dynamic Future Mode and Simple Designed Mode when both are plausible.

For broad, high-impact, or visually ambiguous work, ask the user to choose, combine, or reject options before implementation.

## Do Not

- Do not produce only one direction for broad visual work.
- Do not convert a reference example into the only direction unless the user confirmed it.
- Do not offer decorative directions that ignore the product workflow.
- Do not hide risks; each option must say where it is weak.

## Output

Produce design options using `output/design-options.md`.

If one option is recommended, state why it is recommended and which tradeoff it accepts.

## Stop And Ask

Stop and ask when:

- The user must choose between materially different directions.
- The visual style would drive implementation cost or performance risk.
- The chosen track conflicts with the user's stated platform or workflow.
- A reference image or visual exploration is needed before implementation.
