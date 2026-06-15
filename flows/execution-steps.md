# Flow: Execution Steps

## Purpose

Convert a confirmed or justified design direction into execution-ready frontend design steps.

## When To Read

Read after the user confirms a design direction, or after the agent gives a low-risk recommendation with clear reasoning.

## Inputs

- Requirement summary.
- Chosen track.
- Chosen visual mode.
- Chosen design option or design brief.
- Technical constraints.
- Acceptance criteria.
- Verification requirements.

## Do

Create execution-ready frontend design steps that include:

- Page or screen structure.
- Component breakdown.
- Visual token guidance.
- Motion and interaction rules.
- Responsive behavior rules.
- Recommended implementation order.
- Verification steps.

Use `output/frontend-execution-plan.md`.

## Do Not

- Do not start coding from visual mood alone.
- Do not omit responsive behavior.
- Do not omit verification steps.
- Do not include platform-native implementation claims that V1 cannot support.
- Do not add new functionality that is not traceable to the requirement, selected option, or user confirmation.

## Output

Produce a frontend execution plan that another agent can follow without guessing the intended UI structure.

## Stop And Ask

Stop and ask when:

- The selected design direction is not confirmed.
- Required pages or components are missing.
- Technical stack is unknown and materially affects implementation.
- A requested implementation step is not covered by existing requirements.
- There is a conflict between visual ambition and usability, accessibility, or performance.
