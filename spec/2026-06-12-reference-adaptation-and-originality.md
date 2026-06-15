# Requirement: Reference Adaptation And Originality

## Source Request

User stated on 2026-06-12:

> 我的目标是把别人有用的相关内容改写成适合我的东西，但是也要有自己的东西，不能完全照抄别人的

## New Requirement

The skill must use external and installed skill references as learning material, not as text to copy.

When the skill borrows useful ideas from references, it must transform them into the user's own frontend design workflow, vocabulary, decision rules, and output format.

The skill must also add original structure where needed, especially around:

- Requirement-document intake.
- Product and platform classification.
- Dynamic Future Mode.
- Simple Designed Mode.
- Design option generation.
- Requirement-to-design traceability.
- Execution-ready frontend design steps.
- Verification and QA.

## Required Adaptation Rules

- Extract principles, not prose.
- Rewrite reference ideas in the user's own skill language.
- Combine multiple references into one coherent workflow instead of mirroring any single source.
- Keep only ideas that support the user's goal.
- Add original decision rules when the references are incomplete for this user's goal.
- Avoid copying examples, section structures, phrases, templates, or distinctive wording from reference skills or websites.
- If a reference is used, state its role conceptually rather than reproducing its content.

## Affected Files Or Folders

- `spec/frontend-skill-v1-requirements.md`
- `plan/frontend-skill-v1-implementation-plan.md`
- Future `SKILL.md`
- Future `reference/reference-adaptation.md`
- Future `reference/workflow.md`

## Acceptance Criteria

- V1 requirements include a reference adaptation and originality section.
- V1 implementation plan creates a dedicated reference adaptation document.
- `SKILL.md` reading order includes the reference adaptation rules.
- The workflow requires synthesis from references rather than copying.
- The final skill contains original decision rules tied to this user's frontend design goal.

## Conflict Check

No conflict found with existing requirements.

This requirement constrains how references are used; it does not remove the requirement to study useful existing skills and frontend references.
