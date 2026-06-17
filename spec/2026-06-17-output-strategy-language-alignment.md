# Output Strategy Language Alignment Requirement

## Background

The skill now routes frontend design work through `tracks/`, `strategy/`, `modes/`, `language/`, `rules/`, and `output/`.

The output templates do not yet require agents to expose strategy selection, product-fit evidence, user design language interpretation, or conflicts between user language and product strategy. This can hide the reasoning that the newer layers are meant to provide.

## Requirement

- Update the four active output templates so final deliverables reflect strategy and language reasoning.
- Require outputs to include primary strategy, optional secondary strategy, product-fit evidence, user language interpretation, and strategy-language conflicts where relevant.
- Keep outputs practical and not overly verbose.
- Preserve the current output template roles.

## Scope

- Modify `output/requirement-summary.md`.
- Modify `output/design-options.md`.
- Modify `output/design-brief.md`.
- Modify `output/frontend-execution-plan.md`.
- Create this requirement file.
- Create the matching plan file.

## Out Of Scope

- Do not modify `SKILL.md`.
- Do not modify `README.md`.
- Do not modify `flows/`, `tracks/`, `strategy/`, `modes/`, `language/`, `rules/`, `examples/`, `evals/`, or `reference/`.
- Do not create scripts.
- Do not delete files.

## Acceptance Criteria

- Requirement summary includes strategy readiness and user language interpretation.
- Design options include primary/secondary strategy, product-fit evidence, and strategy-language tradeoffs.
- Design brief includes confirmed strategy and language interpretation decisions.
- Frontend execution plan traces implementation tasks to requirements, strategy, language interpretation, and design brief.
