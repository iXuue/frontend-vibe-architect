# Evals Behavior Layer Requirement

## Background

The skill now has active routing, workflow, track, mode, rule, output, and example layers.

It still needs a lightweight behavior evaluation layer so future changes can be checked against typical user requests. The evaluation layer should describe expected routing and failure conditions without becoming another template library.

## Requirement

- Add an `evals/` folder for behavior-oriented Markdown evals.
- Each eval must describe a realistic user input and the expected skill behavior.
- Evals must check routing, track choice, mode choice, rule use, output template use, stop conditions, and forbidden behavior.
- Evals must not provide final design answers or fixed UI templates.
- Evals must not modify the active runtime layers.

## Eval File Requirements

Each eval file must include:

- User input.
- Expected routing.
- Expected track.
- Expected modes.
- Expected rules.
- Expected output templates.
- Must ask before proceeding.
- Must not do.
- Passing output should include.

## Initial Eval Set

- Web product AI tool.
- Landing brand page.
- Mobile app direction.
- Vague visual reference.
- Conflicting requirements.
- Implementation before design.

## Acceptance Criteria

- `evals/README.md` explains the purpose and usage of the eval layer.
- Six eval files exist with consistent structure.
- The eval layer helps detect whether the skill follows its own routing and stop conditions.
- No existing runtime layer files are modified by this change.
