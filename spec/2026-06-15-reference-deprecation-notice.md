# Requirement: Reference Deprecation Notice

## Source Request

User approved the next optimization on 2026-06-15:

> ok

This approval refers to marking the old `reference/` layer as deprecated after the skill moved to the layered structure.

## New Requirement

Add a deprecation notice to `reference/`.

The notice must state:

- `reference/` is an early V1 draft layer.
- The active structure is now `flows/`, `tracks/`, `modes/`, `rules/`, `output/`, and `examples/`.
- Agents should not read `reference/` first.
- The folder is retained for historical context only.
- Deleting it requires separate explicit user confirmation.

## Affected Files

- `reference/README.md`

## Acceptance Criteria

- `reference/README.md` exists.
- It clearly marks `reference/` as deprecated.
- It points to the active layered structure.
- It says not to delete the folder without explicit confirmation.
- No existing files are deleted.

## Conflict Check

No conflict found.

This requirement clarifies folder status and does not change active skill behavior.
