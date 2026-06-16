# Eval: Vague Visual Reference

## User Input

Make me a website with that futuristic glassy vibe, like the kind of sleek interface I mentioned before. I want it to look expensive and dynamic.

## Expected Routing

- Read `flows/intake.md`.
- Produce `output/requirement-summary.md`.
- Read `rules/examples-are-not-requirements.md`.
- Read `rules/reference-adaptation.md`.
- Stop before choosing a final track if the product type is unknown.

## Expected Track

- No final track should be chosen until the product type is clarified.
- Possible tracks may be listed as candidates only.

## Expected Strategy

- No final strategy should be chosen until product goal, target platform, users, and required screens or workflows are clarified.
- Possible strategies may be listed only as examples of what could change after clarification.
- Do not choose `strategy/immersive-first.md`, `strategy/expression-first.md`, or any other strategy solely from words like "futuristic", "glassy", "expensive", or "dynamic".

## Expected Modes

- `modes/dynamic-future.md` may be considered as a candidate.
- `modes/simple-designed.md` may be offered as a lower-complexity alternative.
- No mode should be treated as mandatory from the vague reference alone.

## Expected Rules

- `rules/examples-are-not-requirements.md`.
- `rules/reference-adaptation.md`.
- `rules/animation.md` if dynamic behavior is discussed.

## Expected Output Templates

- `output/requirement-summary.md`.
- `output/design-options.md` only after product type and target platform are clarified or safely assumed.

## Must Ask Before Proceeding

- What product or website this is for.
- Target platform and primary user.
- Required pages or workflows.
- Whether the glassy/futuristic language is a strict requirement or only a reference for feeling.

## Must Not Do

- Do not assume this is a landing page.
- Do not treat a material style as the whole requirement.
- Do not implement immediately.
- Do not copy a named or implied system style.

## Passing Output Should Include

- A clear explanation that the visual reference is not enough to design the product.
- A short requirement summary with unknowns called out.
- A concise clarification question before design options or implementation.
