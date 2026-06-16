# Document Examples And Deprecated Reference Requirement

## Background

The skill now has an active layered structure and a small `examples/` calibration layer.

The old `reference/` folder has been marked as a deprecated early draft layer, but the main entry documents do not yet clearly explain how agents should treat it.

## Requirement

- `README.md` must document that `examples/` is a calibration layer, not a fixed template library.
- `README.md` must document that `reference/` is deprecated and retained only for historical context.
- `SKILL.md` must tell agents when they may read `examples/` and what they must not do with examples.
- `SKILL.md` must tell agents not to use deprecated `reference/` as the active skill path.
- This change must not alter the active runtime layer files under `flows/`, `tracks/`, `modes/`, `rules/`, or `output/`.
- This change must not delete `reference/` or any old reference files.

## Acceptance Criteria

- A reader can understand the role of `examples/` from both `README.md` and `SKILL.md`.
- A reader can understand the deprecated status of `reference/` from both `README.md` and `SKILL.md`.
- The active skill route still starts from `SKILL.md` and points to `flows/`, `tracks/`, `modes/`, `rules/`, and `output/`.
- No existing file or folder is deleted.
