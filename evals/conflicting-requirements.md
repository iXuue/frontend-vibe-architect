# Eval: Conflicting Requirements

## User Input

Build a dashboard for financial analysts. It should show lots of dense market data and be very fast to scan, but I also want heavy cinematic animations, large immersive sections, and a very decorative futuristic style.

## Expected Routing

- Read `flows/intake.md`.
- Produce `output/requirement-summary.md`.
- Read `flows/choose-track.md`.
- Read `tracks/data-visualization.md`.
- Read `tracks/web-product.md` if the dashboard is app-like.
- Read `rules/animation.md`.
- Stop or ask before committing to a motion-heavy visual direction.

## Expected Track

- Primary: `tracks/data-visualization.md`.
- Secondary: `tracks/web-product.md`.

## Expected Modes

- Prefer `modes/simple-designed.md` for scan speed, density, and analyst workflow.
- Consider `modes/dynamic-future.md` only for limited hierarchy, transitions, or status feedback.

## Expected Rules

- `rules/animation.md`.
- `rules/reference-adaptation.md`.
- `rules/verification.md` if implementation quality is claimed.

## Expected Output Templates

- `output/requirement-summary.md`.
- `output/design-options.md` with explicit tradeoffs.
- `output/design-brief.md` after the user chooses whether clarity or spectacle wins.

## Must Ask Before Proceeding

- Whether scan speed and dense data are higher priority than cinematic motion.
- Which data views are mission-critical.
- Whether decorative motion can be limited to non-critical areas.

## Must Not Do

- Do not force a motion-heavy future style onto dense operational work.
- Do not hide the conflict between data readability and cinematic effects.
- Do not claim the result is analyst-friendly without verification.

## Passing Output Should Include

- A conflict section in the requirement summary.
- A recommendation that protects readability and scan speed.
- Options that make the clarity-versus-impact tradeoff explicit.
- A stop condition or user decision gate before implementation.
