# User Design Language Layer Requirement

## Background

Users often describe frontend design goals with non-professional, subjective, or example-based language.

Examples include "premium", "clean", "dynamic", "simple but designed", "not too plain", "like that product's feeling", "warm", "sharp", "stable", "playful", "high-end", or "with texture".

The skill needs a layer that helps agents translate this language into design variables, clarification questions, risks, and output guidance before choosing tracks, modes, or implementation details.

## Requirement

- Add a `language/` layer for interpreting user design language.
- The layer must not focus on a single style such as futuristic design.
- The layer must help translate vague design language into concrete frontend design decisions.
- The layer must not treat subjective aesthetic words as hard requirements by default.
- The layer must not replace `tracks/`, `modes/`, `rules/`, or `output/`.

## Initial Files

- `language/README.md`
- `language/user-visual-language.md`
- `language/product-tone-language.md`
- `language/layout-language.md`
- `language/motion-language.md`
- `language/material-language.md`
- `language/interaction-language.md`
- `language/ambiguity-patterns.md`

## File Structure Requirement

Each topic file should include:

- Use When
- What User Might Say
- What It May Mean
- What It Does Not Necessarily Mean
- Clarifying Questions
- Design Variables To Adjust
- Suitable Tracks
- Suitable Modes
- Risks
- Output Guidance

## Acceptance Criteria

- The `language/` layer covers broad user design language, not only futuristic or glass-like styles.
- The layer helps agents ask better questions and make better design translations.
- The layer warns against over-interpreting words such as "premium", "simple", "dynamic", or "clean".
- No existing runtime layer files are modified by this change.
