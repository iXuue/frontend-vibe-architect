# Frontend Future Design Skill Next Requirements

## 1. Goal

Define the requirements for the next version after V1. This version should make the skill more reliable at reading requirement documents and translating them into frontend design options, execution steps, mobile apps, mini programs, desktop software, platform-specific design patterns, and reference-image workflows.

## 2. Scope

The next version should extend V1 rather than replace it.

It should add:

- Richer requirement document intake.
- Requirement traceability from source document to design decisions.
- Platform-specific references.
- More complete multi-option design workflow.
- Reference image generation workflow.
- Native mobile and desktop design constraints.
- Mini program constraints.
- Stronger design-system output.
- More robust QA.

## 2.1 Requirement Document Intake

The next version must support richer requirement documents.

It should extract:

- Product goal.
- User roles.
- Target platforms.
- Required pages or screens.
- Core user workflows.
- Content requirements.
- Brand constraints.
- Technical constraints.
- Accessibility constraints.
- Acceptance criteria.
- Open questions.
- Conflicting requirements.

It should produce a requirement summary before design direction generation.

If requirements conflict, the skill must stop and ask the user which requirement wins.

## 3. Platform Expansion

The next version must add detailed platform rules for:

- iOS app direction.
- Android app direction.
- WeChat mini program direction.
- Desktop software direction.
- Large screen dashboard direction.

Each platform rule must include:

- Navigation model.
- Input model.
- Density.
- Motion tolerance.
- Safe areas or viewport constraints.
- Typical anti-patterns.
- What the skill can and cannot promise.

## 4. Reference Image Workflow

The next version must define when and how to create reference images.

It must support:

- Text-only direction when the task is low risk.
- Reference-image prompt when visual ambiguity is high.
- Multiple reference images for broad brand or landing page work.
- Separate references for dynamic future and simple designed modes.
- A conversion step from reference image to tokens, layout, and components.

## 5. Design Option Workflow

The next version must formalize option generation.

Each option must include:

- Target user.
- Product job.
- Visual signature.
- Layout model.
- Material model.
- Typography model.
- Motion model.
- Implementation stack.
- Complexity rating.
- Maintenance risk.
- Accessibility risk.

## 6. Implementation Stack Guidance

The next version must recommend implementation stacks based on scope:

- Static HTML/CSS for very small static pages.
- React/Vite for complex web apps.
- Next.js for routing, SSR, content, and production web apps.
- GSAP for advanced web animation.
- Three.js only when real 3D is necessary.
- Native or platform-specific guidance when implementation is outside Web.

## 7. Stronger Verification

The next version must define QA procedures for:

- Desktop viewport.
- Mobile viewport.
- Reduced motion.
- Low-performance fallback.
- Text overflow.
- Contrast.
- Keyboard navigation.
- Console errors.
- Dynamic effect non-blank rendering.

## 8. Acceptance Criteria

The next version is acceptable when:

- Platform rules exist for Web, mobile, mini program, desktop, and large screen.
- Reference-image workflow is explicit.
- Design option schema is explicit.
- Stack recommendation rules exist.
- Verification is broader than V1.
- Requirement change-control continues to apply.
