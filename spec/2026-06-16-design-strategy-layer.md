# Design Strategy Layer Requirement

## Background

The skill can already classify frontend requests by track and interpret user design language.

It still needs an explicit strategy layer between `tracks/` and `modes/` to infer the design priority from the product requirements. This prevents style from being chosen only from user adjectives or visual references.

## Requirement

- Add a `strategy/` layer for requirement-derived design strategy.
- Strategies must be selected after requirement summary and track choice.
- Strategies must guide mode choice, language interpretation, output recommendations, and implementation planning.
- A product may have one primary strategy and one secondary strategy when justified.
- Strategies must not replace `tracks/`, `modes/`, `rules/`, `language/`, or `output/`.

## Initial Strategies

- `efficiency-first.md`
- `trust-first.md`
- `conversion-first.md`
- `exploration-first.md`
- `expression-first.md`
- `data-insight-first.md`
- `immersive-first.md`

## File Structure Requirement

Each strategy file must include:

- Use When
- Product Fit
- Poor Fit
- Design Priority
- Layout Tendency
- Visual Tendency
- Motion Tendency
- Interaction Tendency
- Suitable Tracks
- Suitable Modes
- Language Interpretation
- Risks
- Output Guidance

## Acceptance Criteria

- `strategy/README.md` explains the layer's role and how it connects tracks, modes, language, and output.
- Seven strategy files exist with consistent structure.
- The strategy layer supports requirement-first style decisions.
- No existing runtime layer files are modified by this change.
