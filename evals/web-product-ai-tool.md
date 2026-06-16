# Eval: Web Product AI Tool

## User Input

I want to build a web app for an AI writing workspace. It should feel advanced and polished, but it needs to be usable every day. It needs a document editor, prompt panel, history, model settings, and output comparison.

## Expected Routing

- Read `flows/intake.md`.
- Produce `output/requirement-summary.md`.
- Read `flows/choose-track.md`.
- Read `tracks/web-product.md`.
- Read `rules/reference-adaptation.md`.
- Read `rules/animation.md` if dynamic interaction is proposed.
- Generate design options before implementation.

## Expected Track

- Primary: `tracks/web-product.md`.
- Secondary: `tracks/desktop-direction.md` may be considered if the interface is dense and editor-like.

## Expected Strategy

- Primary: `strategy/efficiency-first.md` because the product is a repeated-use writing workspace with editor, history, model settings, and comparison workflows.
- Secondary: `strategy/expression-first.md` may be considered only for controlled product personality and polish.
- Do not choose `strategy/immersive-first.md` as the primary strategy unless the requirement changes from daily work tool to presentation or demo experience.

## Expected Modes

- Consider `modes/simple-designed.md` for daily usability and dense work.
- Consider `modes/dynamic-future.md` only as a controlled secondary direction for polish, feedback, and advanced interaction.

## Expected Rules

- `rules/reference-adaptation.md`.
- `rules/animation.md` if motion is included.
- `rules/verification.md` if implementation quality is claimed.

## Expected Output Templates

- `output/requirement-summary.md`.
- `output/design-options.md`.
- `output/design-brief.md` after direction confirmation or justified low-risk recommendation.
- `output/frontend-execution-plan.md` only when implementation planning is requested.

## Must Ask Before Proceeding

- Whether this is a web-only product or should also account for desktop app behavior.
- Which screens are required for the first version if the scope is too large.
- Whether the user prefers productivity density or stronger visual atmosphere if both are plausible.

## Must Not Do

- Do not make a marketing landing page as the primary interface.
- Do not overuse motion in the editor or comparison workflow.
- Do not start implementation before the product workflow and design direction are clear.

## Passing Output Should Include

- A requirement summary that separates confirmed screens from assumptions.
- A web product track choice with rationale.
- At least two design options if the visual direction remains broad.
- A clear tradeoff between visual impact and daily-use clarity.
