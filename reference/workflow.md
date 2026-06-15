# Workflow

## Step 0: Requirement Document Intake

Read the user's requirement document or treat the user's message as a lightweight requirement document.

Supported V1 input forms:

- Plain text pasted by the user.
- Markdown requirement documents.
- Local `.md` or `.txt` files when the user provides an explicit path.
- Short user messages that can be normalized into a lightweight requirement document.

V1 does not promise automatic parsing of Word documents, PDFs, images, Figma files, or external product docs unless a later requirement explicitly adds that capability.

Extract:

- Product goal.
- Target users.
- Target platform.
- Required pages or screens.
- Core workflows.
- Content constraints.
- Visual constraints.
- Technical constraints.
- Accessibility constraints.
- Acceptance criteria.
- Open questions.
- Potential conflicts.

Before proposing visual directions, summarize the interpreted requirement. If a material requirement is unclear and the answer would change scope, architecture, platform, or acceptance criteria, ask the user before proceeding.

## Step 1: Understand

Identify:

- Product type.
- Target user.
- Primary user job.
- Platform.
- Brand/product classification.
- Time horizon: quick browsing, long-use tool, presentation, creation, monitoring, transaction.

Do not treat every request as a landing page. Operational tools, dashboards, admin systems, and creative tools should prioritize task flow, density, state clarity, and repeated-use ergonomics.

## Step 2: Classify

Classify as one:

- Brand surface.
- Product surface.
- Hybrid surface.

Brand surfaces can use stronger visual signature and narrative pacing. Product surfaces need clearer controls, stable layout, lower friction, and stricter verification. Hybrid surfaces must state which part is brand-led and which part is workflow-led.

## Step 3: Generate Options

Offer 2-4 options. Each option must include:

- Name.
- Best-fit scenario.
- Visual language.
- Layout strategy.
- Color and material strategy.
- Motion strategy.
- Reference image direction.
- Implementation difficulty.
- Risks.

Include both Dynamic Future Mode and Simple Designed Mode when both are plausible. Do not force future styling onto tools where clarity, scanning, or repeated use matters more.

## Step 4: Ask for Direction

If the request is broad, high-impact, or visually ambiguous, ask the user to choose or combine options before implementation.

For small, low-risk tasks, recommend one direction directly while briefly explaining the rejected alternatives.

## Step 5: Convert Direction to Build Spec

After direction confirmation or low-risk recommendation, produce:

- Design brief.
- Tokens.
- Component language.
- Motion language.
- Page or screen structure.
- Execution-ready frontend design steps.
- Verification checklist.

Execution-ready frontend design steps must include:

- Page or screen structure.
- Component breakdown.
- Visual token guidance.
- Motion and interaction rules.
- Responsive behavior rules.
- Recommended implementation order.
- Verification steps.
