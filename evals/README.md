# Evals

This folder contains behavior evals for `frontend-vibe-architect`.

Use these files to check whether the skill follows its intended routing, stop conditions, and output contracts when given typical frontend requests.

## What Evals Are

- Behavior checks for the skill.
- Inputs that represent common or risky user requests.
- Expected routing through `flows/`, `tracks/`, `modes/`, `rules/`, and `output/`.
- Guardrails against copying examples, skipping requirement summary, or implementing too early.

## What Evals Are Not

- They are not finished UI designs.
- They are not visual templates.
- They are not prompt snippets to copy into final answers.
- They are not replacements for rendered UI verification when code is produced.

## Required Eval Shape

Each eval should use this structure:

```markdown
# Eval: [Name]

## User Input

## Expected Routing

## Expected Track

## Expected Strategy

## Expected Modes

## Expected Rules

## Expected Output Templates

## Must Ask Before Proceeding

## Must Not Do

## Passing Output Should Include
```

## How To Use

1. Read the eval input.
2. Run the request through `SKILL.md`.
3. Compare the agent behavior to the expected routing and stop conditions.
4. Treat missing required routing, skipped questions, copied examples, or unverified implementation claims as failures.
