# Requirement: Examples Are Not Requirements

## Source Request

User clarified on 2026-06-12:

> 磨玻璃/半透明材质风格规则也是我说的一种例子

The user also clarified that a named operating system or product style can be only an example used to express a design feeling, not a required design source.

## New Requirement

The skill must not convert user examples into fixed requirements.

When the user uses informal, non-professional, example-based visual language, the skill must separate:

- Hard requirements.
- Reference examples.
- Visual intent.
- Forbidden directions.
- Agent assumptions.
- Questions that need confirmation.

Examples such as a named operating system, a product style, frosted material, translucent material, cinematic motion, or a design trend must be treated as reference clues only unless the user explicitly says that the example is a required style.

## Required Behavior

- Do not create a dedicated rule file for a single user-provided example.
- Do not hard-code a named product, operating system, design trend, or material as a required design direction.
- Translate examples into design variables such as hierarchy, density, motion intensity, atmosphere, material depth, contrast, readability, and interaction feedback.
- Generate multiple design directions from those variables.
- Ask for confirmation before upgrading an example into a hard design constraint.

## Affected Files Or Folders

- `SKILL.md`
- `flows/intake.md`
- `rules/examples-are-not-requirements.md`
- `spec/frontend-skill-v1-requirements.md`
- `spec/2026-06-12-layered-skill-structure.md`
- `plan/frontend-skill-v1-layered-restructure-plan.md`
- Removed dedicated rule files for a single named visual example.

## Acceptance Criteria

- No active skill file contains a dedicated rule for a single named product, operating system, trend, material, or visual effect.
- No active skill file makes frosted glass, translucent material, or any single visual example a required design direction.
- A new rule exists for separating hard requirements from reference examples.
- Requirement intake requires translating informal visual examples into design variables.
- The skill asks for confirmation before treating an example as a hard constraint.

## Conflict Check

This requirement intentionally supersedes earlier requirements that promoted a single user example into a design boundary.

The earlier example-specific requirement was too specific and incorrectly promoted a user example into a formal design rule.
