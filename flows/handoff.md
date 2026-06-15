# Flow: Handoff

## Purpose

Package the result into the right final response for the current request stage.

## When To Read

Read before final response, whether the work is design-only, planning-only, or implementation-ready.

## Inputs

- Requirement summary.
- Chosen track and visual mode.
- Design options or chosen design brief.
- Execution-ready frontend design steps, if produced.
- Verification checklist, if implementation happened or is ready to happen.
- Risks, assumptions, and user confirmations.

## Do

For design-only work, hand off:

- Requirement summary.
- Chosen track and visual mode.
- Design options or chosen design brief.
- Risks and assumptions.

For implementation-ready work, also hand off:

- Execution-ready frontend design steps.
- Verification checklist.
- Required browser or visual QA.

If implementation has already happened, verify with `rules/verification.md` before final response.

## Do Not

- Do not imply implementation happened when only design planning happened.
- Do not hide unresolved questions.
- Do not omit risk when a visual direction is costly, ambiguous, or performance-sensitive.
- Do not present a direction as user-approved unless the user actually confirmed it.

## Output

Produce a final response that clearly states:

- What was understood.
- What was decided.
- What remains open.
- What the next execution step is.

## Stop And Ask

Stop and ask when:

- The user has not approved a broad design direction.
- A conflict remains unresolved.
- The final response would require claiming implementation or verification that was not performed.
