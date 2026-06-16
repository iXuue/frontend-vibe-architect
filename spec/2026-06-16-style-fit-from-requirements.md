# Style Fit From Requirements Requirement

## Background

The skill now has a `language/` layer for interpreting user design language.

However, user adjectives and style references must not decide the visual direction by themselves. The design direction should first come from the user's requirement document, product type, target users, usage context, task density, platform, risk level, and desired product outcome.

## Requirement

- Add a rule that requires style fit to be inferred from product requirements before user design language is applied.
- Treat user design words as secondary interpretation signals, not the primary style decision source.
- If user language conflicts with product-fit strategy, the agent must explain the conflict and ask the user to choose or offer options.
- Connect this rule to `SKILL.md` routing.
- Clarify in `language/README.md` that `language/` supports requirement-based design decisions and does not override them.

## Scope

- Create `rules/style-fit-from-requirements.md`.
- Modify `SKILL.md`.
- Modify `language/README.md`.
- Create this requirement file.
- Create the matching plan file.

## Out Of Scope

- Do not modify `tracks/`, `modes/`, `output/`, `examples/`, `evals/`, or `reference/`.
- Do not create scripts.
- Do not delete files.

## Acceptance Criteria

- `rules/style-fit-from-requirements.md` clearly states the decision order: requirements first, language second.
- `SKILL.md` routes vague design language through requirement summary, track choice, style-fit rule, and then relevant `language/` files.
- `language/README.md` warns that language interpretation must not override product-fit reasoning.
- The rule handles conflicts between user words and product needs.
