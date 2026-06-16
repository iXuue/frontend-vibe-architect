# Interaction Language

## Use When

Use when the user talks about ease of use, responsiveness, control, smoothness, intuitive behavior, workflow efficiency, or product feel during use.

## What User Might Say

- It should be easy to use.
- Make it intuitive.
- It should feel smooth.
- Users should feel in control.
- It needs to be efficient.
- I want it to feel polished when clicking around.

## What It May Mean

- Clear affordances.
- Predictable navigation.
- Visible system status.
- Useful loading and error states.
- Strong hover, focus, active, selected, disabled, and empty states.
- Low friction for repeated workflows.
- Good keyboard, pointer, or touch behavior depending on platform.

## What It Does Not Necessarily Mean

- Fewer features.
- Hidden controls.
- Unlabeled icons.
- Animation on every action.
- Novel navigation.
- Removing confirmation or safety steps.

## Clarifying Questions

- What is the most repeated workflow?
- What mistakes should the interface prevent?
- Should the user optimize for speed, confidence, creativity, or exploration?
- Does the interface need keyboard, touch, or pointer-first behavior?

## Design Variables To Adjust

- Control placement.
- Button hierarchy.
- Form behavior.
- State visibility.
- Feedback timing.
- Confirmation flows.
- Undo or recovery paths.
- Keyboard and focus behavior.
- Touch target size.

## Suitable Tracks

- `tracks/web-product.md` for workflow-heavy tools.
- `tracks/mobile-direction.md` for touch-first flows.
- `tracks/desktop-direction.md` for professional productivity surfaces.
- `tracks/data-visualization.md` for filtering, comparison, and data exploration.
- `tracks/landing-brand.md` for conversion actions and interactive demos.

## Suitable Modes

- `modes/simple-designed.md` for efficient, clear, repeatable interactions.
- `modes/dynamic-future.md` when advanced interaction is part of the product value and does not reduce control.

## Risks

- Confusing novelty with intuitiveness.
- Hiding controls for visual cleanliness.
- Missing loading, error, disabled, or empty states.
- Making touch targets too small.
- Using motion without functional feedback.

## Output Guidance

- Include expected interaction states in design briefs and execution plans.
- State the primary workflow and interaction priority.
- Specify whether controls are optimized for pointer, touch, keyboard, or mixed use.
- Route implementation claims through verification when UI code exists.
