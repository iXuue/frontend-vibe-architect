# Ambiguity Patterns

## Use When

Use when user design language is too vague, conflicting, example-dependent, or likely to change the design direction if interpreted incorrectly.

## What User Might Say

- Make it look better.
- You understand what I mean.
- Make it like that vibe.
- It should be advanced but simple.
- Not too much, but not boring.
- Make it suitable for my product.
- Just design it yourself.

## What It May Mean

- The user has a desired feeling but has not stated product constraints.
- The request may be missing target users, platform, screens, or workflows.
- The user may be using examples as emotional references, not requirements.
- The user may want the agent to propose options before committing.

## What It Does Not Necessarily Mean

- Permission to invent product scope.
- Permission to implement immediately.
- Permission to copy an implied reference.
- A confirmed visual mode.
- A confirmed track.

## Clarifying Questions

- What product or interface is this for?
- Who will use it, and what are they trying to do?
- Which platform is required?
- What screens or workflows must exist?
- Is the reference a hard requirement or only a feeling?
- Which matters more: clarity, visual impact, speed, trust, or memorability?

## Design Variables To Adjust

- Requirement certainty.
- Track confidence.
- Mode confidence.
- Reference status.
- Stop condition.
- Assumption level.
- Design option breadth.

## Suitable Tracks

- No track should be finalized if product type is unknown.
- Candidate tracks may be listed as possibilities with assumptions.

## Suitable Modes

- No mode should be finalized from vague language alone.
- Candidate modes may be offered only after product context is stated or clearly assumed.

## Risks

- Implementing before requirements exist.
- Treating vague taste language as confirmed design direction.
- Overfitting to one example.
- Hiding uncertainty from the user.
- Producing generic UI because the product is unknown.

## Output Guidance

- Use `output/requirement-summary.md` first.
- Put unclear phrases under visual intent or open questions.
- Ask before proceeding when product goal, platform, screens, workflows, or acceptance criteria are missing.
- Offer design options only after enough context exists to make options meaningful.
