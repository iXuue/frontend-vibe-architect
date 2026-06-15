# Agent Instructions

## Scope

This repository is for building a frontend design skill.

The agent must keep requirements, plans, and implementation aligned.

## Language

Respond in Chinese by default unless the user explicitly asks for another language or when quoting code, commands, logs, or file content.

## Requirement Control

Before modifying implementation files, check whether the requested change is covered by an existing requirement file under `spec/`.

If the requested code change is not covered by current requirements:

1. Create a new requirement note under `spec/`.
2. Name it with the relevant feature and date.
3. Include:
   - User request.
   - New requirement.
   - Affected files or folders.
   - Acceptance criteria.
4. Do not silently expand implementation scope.

If a new requirement conflicts with an earlier requirement:

1. Stop before editing code.
2. Tell the user there is a conflict.
3. Identify the conflicting requirement files.
4. Ask which requirement should win.
5. Continue only after explicit user confirmation.

## Planning Rule

Before substantial code changes, produce or update a plan under `plan/`.

The plan must include:

- Understood requirement.
- Scope.
- Files expected to change.
- Implementation steps.
- Verification steps.
- Risks.

## File Safety

Before modifying or deleting an existing file, back it up under `E:\codex_backup`.

Do not delete files without explicit user confirmation.

## Current Planned Documents

- `spec/frontend-skill-v1-requirements.md`
- `plan/frontend-skill-v1-implementation-plan.md`
- `spec/frontend-skill-next-requirements.md`
- `plan/frontend-skill-next-implementation-plan.md`

