# Frontend Future Design Skill V1 Requirements

## 1. Goal

Create the first version of a frontend design skill that helps an agent read a user's requirement document, understand the frontend product need, design product-appropriate interface options, and produce execution-ready frontend design steps before implementation.

The skill must not simply follow a user prompt literally. It must interpret the product need, classify the frontend surface, propose design options, and guide implementation only after the direction is clear.

## 2. Design Positioning

The skill is a requirement-document-driven design-decision system for frontend interfaces.

V1 must be structured as a layered, callable skill rather than a flat reference collection.

Required layers:

- Entry layer: `SKILL.md` as compact trigger and router.
- Flow layer: requirement intake, track selection, option generation, execution-step conversion, and handoff.
- Track layer: product/platform-specific design paths.
- Mode layer: dynamic future and simple designed visual modes.
- Rule layer: reference adaptation, examples-are-not-requirements, animation, verification, and requirement change control.
- Output layer: reusable response templates.

The primary V1 input is a user requirement document or a user message that can be treated as a lightweight requirement document.

V1 supports these requirement input forms:

- Plain text pasted by the user.
- Markdown requirement documents.
- Local `.md` or `.txt` files when the user provides an explicit path.
- Short user messages that can be normalized into a lightweight requirement document.

V1 does not promise automatic parsing of Word documents, PDFs, images, Figma files, or external product docs unless a later requirement explicitly adds that capability.

The primary V1 output is:

- Structured understanding of the requirement.
- Multiple design directions.
- A recommended or user-selected design brief.
- Frontend execution steps.
- Verification steps.

It should support:

- Websites and landing pages.
- Web apps and SaaS tools.
- Dashboards and admin panels.
- AI tools and creative tools.
- Data visualization and monitoring pages.
- Initial direction for mobile apps, mini programs, and desktop software.

V1 is strongest for Web and React-style frontend work. Non-Web platforms are supported as design direction only in V1, not as complete native platform specification.

## 3. Required Reference Sources

The skill must explicitly use these installed skills as reference material:

- `impeccable`: overall frontend design workflow, product/brand distinction, critique, polish, animation, layout, typography, color, quality gates.
- `frontend-design`: distinctive visual direction, anti-template rules, design plan before implementation.
- `ui-ux-pro-max`: UI/UX rules, product types, accessibility, layout, typography, color, platform guidance.
- `canvas-design`: visual philosophy and reference-image direction.
- `algorithmic-art`: dynamic visual systems such as particles, flow fields, generated backgrounds, and data-driven atmosphere.
- `theme-factory`: theme and palette candidate structure.
- `gsap-*`: animation implementation references for core animation, timelines, ScrollTrigger, plugins, React, performance, utilities, and framework adaptation.
- `webapp-testing`: browser validation and visual QA.

## 3.1 Reference Adaptation And Originality

The skill must learn from useful existing references, but it must not copy them directly.

Required behavior:

- Extract reusable principles from reference skills, websites, and design examples.
- Rewrite those principles into the user's own frontend design workflow and vocabulary.
- Combine multiple references into one coherent system rather than mirroring any single source.
- Add original decision rules that fit this skill's goal: reading requirement documents, producing design options, and creating execution-ready frontend design steps.
- Keep only reference ideas that help the user's target use cases.
- Avoid copying distinctive examples, section structures, wording, prompts, or templates from reference sources.

The first version must contain original structure around:

- Requirement-document intake.
- Product and platform classification.
- Dynamic Future Mode.
- Simple Designed Mode.
- Design option generation.
- Requirement-to-design conversion.
- Verification and QA.

## 4. Examples Are Not Requirements

The skill must not convert user examples into fixed requirements.

When the user uses informal, non-professional, example-based visual language, the skill must separate:

- Hard requirements.
- Reference examples.
- Visual intent.
- Forbidden directions.
- Agent assumptions.
- Questions that need confirmation.

Examples such as a named operating system, a product style, a material, an interaction effect, or a design trend must be treated as reference clues only unless the user explicitly says that the example is a required style.

The skill must translate examples into design variables such as hierarchy, density, motion intensity, material depth, contrast, readability, atmosphere, interaction feedback, platform fit, and performance tolerance.

## 5. Required Design Modes

The skill must support at least two visual modes:

### 5.1 Dynamic Future Mode

Use when the product benefits from strong visual expression.

Possible traits:

- Spatial depth.
- Generative or data-driven background layers.
- GSAP timeline or scroll animation.
- High-quality hover and state transitions.
- Cinematic landing sections.

Required constraints:

- Motion must serve information or state.
- Provide reduced-motion fallback.
- Provide mobile performance fallback.
- Avoid animation that blocks reading or task completion.

### 5.2 Simple Designed Mode

Use when the interface should be visually simple but still designed.

Traits:

- Fewer materials.
- Fewer animations.
- Strong typography.
- Clear hierarchy.
- Precise spacing.
- One memorable visual element.
- Better suited for tools, dashboards, admin panels, long-use workflows, and productivity products.

This mode is not a rough or plain version. It is a controlled, quieter design direction.

## 6. Required Workflow

For every substantial frontend request, the skill must follow this flow:

1. Read the user requirement document or treat the user message as a lightweight requirement document.
2. Extract product goal, target user, platform, required screens, core workflows, constraints, and acceptance criteria.
3. Identify unresolved questions and material assumptions.
4. Understand the product.
5. Classify the surface.
6. Decide whether the task is `brand` or `product`.
7. Identify audience, primary job, platform, and usage context.
8. Generate 2-4 design directions.
9. Include both dynamic and simple options when appropriate.
10. For each option, include:
   - Name.
   - Suitable scenario.
   - Visual language.
   - Layout strategy.
   - Color/material strategy.
   - Motion strategy.
   - Reference-image suggestion.
   - Implementation difficulty.
   - Risks.
11. Ask the user to choose or refine a direction before implementation if the scope is broad, high-impact, or visually ambiguous.
12. For small, low-risk tasks, the skill may recommend one direction directly while still explaining the rejected alternatives briefly.
13. After direction approval or low-risk recommendation, produce:
   - Design brief.
   - Design tokens.
   - Component language.
   - Motion rules.
   - Implementation notes.
   - Execution-ready frontend design steps.
   - Verification checklist.

Execution-ready frontend design steps must include at least:

- Page or screen structure.
- Component breakdown.
- Visual token guidance.
- Motion and interaction rules.
- Responsive behavior rules.
- Recommended implementation order.
- Verification steps.

## 7. Required Output Types

V1 must support these outputs:

- Requirement interpretation.
- Design direction options.
- Reference image prompt or reference image request.
- Design brief.
- Design token proposal.
- Page or screen structure.
- Component strategy.
- Motion strategy.
- Implementation plan.
- QA checklist.

## 8. Anti-Patterns

The skill must actively avoid:

- Default purple-blue gradients.
- Default dark tech UI.
- Cards inside cards.
- Making every section a card.
- Low-contrast gray text.
- Decorative animation without meaning.
- Generic SaaS hero layouts.
- Inter/system font as the only visual personality.
- Treating a user-provided example as a fixed design requirement without confirmation.

## 9. V1 Acceptance Criteria

V1 is acceptable when:

- It has a clear `SKILL.md`.
- `SKILL.md` acts as an entry/router file rather than a long reference document.
- It separates flow, track, mode, rule, and output template layers.
- It explains when to trigger.
- It includes a concrete workflow.
- It defines dynamic and simple modes.
- It names the installed reference skills and their roles.
- It includes reference adaptation and originality rules.
- It includes examples-are-not-requirements rules.
- It forces option generation before implementation for broad tasks.
- It includes a verification checklist.
- It includes rules for requirement changes and conflict handling.
