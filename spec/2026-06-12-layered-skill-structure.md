# Requirement: Layered Skill Structure

## Source Request

User stated on 2026-06-12 that the first implementation feels unlike a real skill:

> 感觉你写的很不像skill，没有分层，感觉分的不清楚

User then approved the proposed direction:

> 认可

## New Requirement

V1 must be restructured from a flat reference collection into a layered, callable skill.

The skill must separate:

- Entry layer: trigger, routing, mandatory first actions.
- Flow layer: requirement intake, track selection, option generation, execution-step conversion, final handoff.
- Track layer: product/platform-specific design paths.
- Mode layer: visual style modes.
- Rule layer: reference adaptation, examples-are-not-requirements, animation, verification, requirement change control.
- Output layer: fixed response templates for requirement summary, design options, design brief, and frontend execution plan.

## Required File Structure

The V1 implementation should use this structure:

```text
E:\ui-skill
├─ SKILL.md
├─ flows\
│  ├─ intake.md
│  ├─ choose-track.md
│  ├─ design-options.md
│  ├─ execution-steps.md
│  └─ handoff.md
├─ tracks\
│  ├─ web-product.md
│  ├─ landing-brand.md
│  ├─ mobile-direction.md
│  ├─ desktop-direction.md
│  └─ data-visualization.md
├─ modes\
│  ├─ dynamic-future.md
│  └─ simple-designed.md
├─ rules\
│  ├─ reference-adaptation.md
│  ├─ examples-are-not-requirements.md
│  ├─ animation.md
│  ├─ verification.md
│  └─ requirement-change-control.md
└─ output\
   ├─ requirement-summary.md
   ├─ design-options.md
   ├─ design-brief.md
   └─ frontend-execution-plan.md
```

## Behavioral Requirement

`SKILL.md` must behave as a compact router rather than a long reference document.

It must tell the agent to:

1. Read requirement intake flow.
2. Produce a requirement summary.
3. Choose a product/platform track.
4. Choose relevant visual mode files.
5. Generate 2-4 design options.
6. Ask for user direction when scope is broad, high-impact, or visually ambiguous.
7. Convert the selected direction into execution-ready frontend design steps.
8. Use output templates for stable responses.

## Affected Files Or Folders

- `SKILL.md`
- `reference/`
- `flows/`
- `tracks/`
- `modes/`
- `rules/`
- `output/`
- `spec/frontend-skill-v1-requirements.md`
- `plan/frontend-skill-v1-implementation-plan.md`

## Acceptance Criteria

- V1 no longer presents itself as only a set of reference documents.
- `SKILL.md` is an entry/router file.
- Flow, track, mode, rule, and output layers exist as separate folders.
- Each file has one clear responsibility.
- Output templates exist and are referenced by the flow.
- The old `reference/` layer is not the primary structure anymore.
- No existing requirement is weakened: requirement-document intake, reference adaptation, examples-are-not-requirements, dynamic/simple modes, execution steps, verification, and change control remain covered.

## Conflict Check

No conflict found.

This requirement refines the internal structure of V1. It does not change the product goal or remove any prior requirement.
