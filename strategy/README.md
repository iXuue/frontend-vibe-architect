# Strategy Layer

The `strategy/` layer translates product requirements into design priorities.

Use it after requirement summary and track selection, before choosing visual modes or interpreting user design language.

## Purpose

- Decide what the interface should optimize for.
- Connect product context to layout, visual, motion, and interaction choices.
- Prevent style from being chosen only from user adjectives.
- Help explain why a design direction fits the product.

## Decision Order

```text
FIRST summarize requirements.
THEN choose primary track and optional secondary track.
THEN choose primary strategy and optional secondary strategy.
THEN choose visual modes.
THEN interpret user design language through language/.
THEN produce design options, design brief, or execution plan.
```

## Strategy Files

- `efficiency-first.md`: repeated task completion, speed, density, and low friction.
- `trust-first.md`: confidence, stability, safety, and serious decision contexts.
- `conversion-first.md`: persuasion, clarity of offer, proof, and action.
- `exploration-first.md`: discovery, browsing, comparison, and optional paths.
- `expression-first.md`: brand personality, creativity, memorability, and emotional impression.
- `data-insight-first.md`: metrics, analysis, monitoring, and sensemaking.
- `immersive-first.md`: atmosphere, narrative, spatial feeling, and high-impact presentation.

## Selection Rules

- Choose strategy from product requirements, not from adjectives alone.
- A product may use one primary strategy and one secondary strategy.
- If strategies conflict, state the tradeoff.
- If user language conflicts with the strategy, explain the conflict and offer options.

## Do Not

- Do not use strategy as a replacement for `tracks/`.
- Do not use strategy as a replacement for `modes/`.
- Do not choose an immersive or expressive strategy just because the user asks for something "cool".
- Do not choose an efficiency strategy if the product's main goal is persuasion or storytelling.
