# Rule: Style Fit From Requirements

## Use When

Use when the user asks for a visual style, aesthetic direction, product feeling, or design tone.

Also use when the user provides subjective design language such as premium, clean, dynamic, simple, playful, calm, futuristic, professional, warm, bold, glassy, immersive, or "like this kind of feeling".

## Rule

Choose design style from product requirements first.

Use user design language as a secondary interpretation signal after the requirement summary and track choice are clear.

## Decision Order

```text
FIRST analyze the requirement document or user request.
THEN identify product type, target users, platform, core workflows, usage frequency, task density, risk level, and success criteria.
THEN choose the primary track and optional secondary track.
THEN infer the product-fit design strategy.
THEN use relevant language/ files to interpret user design words.
THEN generate design options or a design brief.
```

## Product-Fit Signals

- Product category.
- Target user expertise.
- Primary workflow.
- Usage frequency.
- Information density.
- Data sensitivity or decision risk.
- Conversion, trust, efficiency, memorability, or exploration priority.
- Platform constraints.
- Accessibility and readability requirements.
- Available assets and implementation budget.

## If User Language Supports Product Fit

Then use it to tune:

- Visual hierarchy.
- Tone.
- Density.
- Motion level.
- Material treatment.
- Interaction feedback.
- Layout rhythm.
- Brand expression.

## If User Language Conflicts With Product Fit

Then:

1. State the conflict clearly.
2. Explain why the product requirements point in a different direction.
3. Offer design options that expose the tradeoff.
4. Ask the user to choose if the tradeoff materially changes the product.

Examples:

- A dense financial dashboard asks for heavy cinematic animation.
- A daily work tool asks for immersive decorative transitions.
- A trust-sensitive health or finance product asks for playful, chaotic visuals.
- A landing page asks for extreme minimalism but also must explain a complex offer.

## Do

- Treat style as a product decision, not a decoration decision.
- Translate user words into design variables after understanding the product.
- Explain why a style fits the requirement.
- Offer alternatives when user preference and product fit diverge.
- Route vague words through `language/` only after requirement context exists.

## Do Not

- Do not choose style from adjectives before reading requirements.
- Do not let one aesthetic word override product type, user need, or workflow.
- Do not equate a user word with a fixed visual recipe.
- Do not use `language/` as the primary style router.
- Do not hide conflicts between user taste and product usability.

## Stop And Ask

Stop and ask before design options or implementation when:

- Product type is unknown.
- Target platform is unknown and would change design direction.
- Required screens or workflows are missing.
- User style language conflicts with product needs.
- It is unclear whether a style word is a hard requirement or a loose reference.

## Output Impact

- `output/requirement-summary.md` should separate product-fit evidence from user style language.
- `output/design-options.md` should explain how each option fits the requirements and how it interprets user language.
- `output/design-brief.md` should state the chosen product-fit design strategy and any user preference tradeoffs.
- `output/frontend-execution-plan.md` should only implement style decisions that trace back to requirements, confirmed options, or the design brief.
