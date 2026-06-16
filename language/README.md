# Language Layer

The `language/` layer helps interpret user design language after the product requirements are understood.

Use it when the user describes the desired interface with subjective, vague, emotional, example-based, or non-professional wording.

Do not use this layer to choose style before requirement analysis. First summarize the product requirements, choose the relevant track, and apply `rules/style-fit-from-requirements.md`.

## Purpose

- Translate user language into design variables after product-fit reasoning.
- Separate aesthetic intent from hard requirements.
- Identify clarification questions.
- Prevent shallow style mapping.
- Improve track, mode, rule, and output decisions.

## Core Rule

Do not treat user design words as fixed UI recipes.

Translate language into product context, user need, information density, interaction model, visual hierarchy, motion level, material treatment, and verification risks.

`language/` is secondary to requirement-based style fit. If user wording conflicts with product needs, explain the conflict and offer options instead of silently following the wording.

## Topic Files

- `user-visual-language.md`: broad visual words such as premium, clean, playful, bold, calm, sharp, warm, or high-end.
- `product-tone-language.md`: product personality and brand tone.
- `layout-language.md`: structure, density, spacing, hierarchy, and composition.
- `motion-language.md`: dynamic feeling, transitions, feedback, and motion restraint.
- `material-language.md`: texture, depth, transparency, surface, elevation, and visual weight.
- `interaction-language.md`: user control, feedback, state, responsiveness, and affordance.
- `ambiguity-patterns.md`: common vague phrasing and when to stop and ask.

## Usage

1. Read the requirement or user request.
2. Produce a requirement summary.
3. Choose the primary track and optional secondary track.
4. Apply `rules/style-fit-from-requirements.md`.
5. Identify the user's design language.
6. Choose the relevant language file.
7. Translate the wording into adjustable design variables.
8. Decide whether clarification is required.
9. Continue to `modes/`, other `rules/`, and `output/`.

## Do Not

- Do not make one style word drive the whole product.
- Do not equate "premium" with dark UI, glass, gradients, or animation.
- Do not equate "simple" with empty, low-information, or undesigned.
- Do not equate "dynamic" with heavy animation.
- Do not copy products named as references.
