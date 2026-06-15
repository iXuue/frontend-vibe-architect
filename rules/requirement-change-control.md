# Rule: Requirement Change Control

If a requested code change is not covered by the existing requirement documents:

1. Create or append a requirement note under `spec/`.
2. Name it with the relevant feature and date.
3. State the new requirement, source request, affected files, and acceptance criteria.
4. Do not silently expand implementation scope.

If the new requirement conflicts with an earlier requirement:

1. Stop before editing code.
2. Explain the conflict to the user.
3. Name the conflicting requirement files.
4. Ask the user which requirement wins.
5. Proceed only after explicit user confirmation.

Do not delete files or folders without explicit user confirmation.
