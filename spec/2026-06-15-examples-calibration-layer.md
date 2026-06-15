# Requirement: Examples Calibration Layer

## Source Request

User approved adding a small examples layer on 2026-06-15:

> ok

This approval refers to adding a small calibration layer after comparing mature skills that use examples, references, assets, or scripts to guide agent behavior.

## New Requirement

Add a lightweight `examples/` layer with three calibration examples.

The examples must demonstrate how the skill routes real user requests through:

- Requirement intake.
- Track selection.
- Mode selection.
- Rule selection.
- Output template selection.

The examples must not become mandatory recipes. They are calibration references for expected routing and output shape.

## Required Examples

- `examples/web-product-ai-tool.md`
- `examples/landing-brand-page.md`
- `examples/informal-visual-example.md`

Each example must include:

- User Request.
- Expected Routing.
- Expected Requirement Interpretation.
- Expected Design Direction Shape.
- Expected Output Shape.
- Notes On What Not To Do.

## Acceptance Criteria

- `examples/` exists.
- The three required example files exist.
- Each example shows how to combine flow, track, mode, rule, and output layers.
- The informal visual example demonstrates that user examples are not hard requirements.
- No existing core layer files are changed in this pass.

## Conflict Check

No conflict found.

This requirement adds calibration examples and does not change the skill's routing or design rules.
