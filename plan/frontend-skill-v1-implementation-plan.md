# Frontend Future Design Skill V1 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build the first version of a frontend design skill that reads user requirement documents, adapts useful reference material into the user's own design system, classifies frontend needs, proposes product-appropriate visual directions, and produces execution-ready frontend design steps with dynamic future and simple designed modes.

**Architecture:** The skill should be a compact instruction package centered on one `SKILL.md`, supported by focused reference documents for workflow, platform classification, visual modes, Examples Are Not Requirements inspiration, animation guidance, and verification. V1 should avoid executable scripts unless a later requirement proves they are needed.

**Tech Stack:** Markdown-based Agent Skill, local files under `E:\ui-skill`, references to installed global skills, no runtime dependencies in V1.

---

## File Structure

- Create: `E:\ui-skill\SKILL.md`
  - Main trigger description, mandatory workflow, output format, anti-patterns, and reference-skill routing.
- Create: `E:\ui-skill\reference\workflow.md`
  - Step-by-step requirement-document intake and design decision workflow.
- Create: `E:\ui-skill\reference\reference-adaptation.md`
  - Rules for learning from existing useful references without copying their prose, templates, or structure directly.
- Create: `E:\ui-skill\reference\visual-modes.md`
  - Dynamic Future Mode and Simple Designed Mode rules.
- Create: `E:\ui-skill\reference\examples-examples-are-not-requirements.md`
  - examples-are-not-requirements rules.
- Create: `E:\ui-skill\reference\platform-scenarios.md`
  - V1 platform classification rules.
- Create: `E:\ui-skill\reference\animation.md`
  - GSAP usage guidance and reduced-motion/performance rules.
- Create: `E:\ui-skill\reference\verification.md`
  - Browser and design QA checklist.
- Create: `E:\ui-skill\reference\requirement-change-control.md`
  - Requirement drift and conflict-handling policy.

## Task 1: Create Main Skill File

**Files:**
- Create: `E:\ui-skill\SKILL.md`

- [ ] **Step 1: Create `SKILL.md` with trigger metadata**

Write:

```markdown
---
name: frontend-future-design
description: Use when the user wants a frontend interface designed, redesigned, planned, critiqued, or implemented across websites, web apps, dashboards, AI tools, mobile app directions, mini program directions, or desktop software directions. The skill classifies the product need, proposes multiple design directions, supports dynamic future and simple designed modes, references examples-are-not-requirements rules, and guides implementation with animation and verification rules.
---

# Frontend Future Design

Use this skill to design product-appropriate frontend interfaces before implementation.
```

- [ ] **Step 2: Add required reading order**

Append:

```markdown
## Required Reading Order

1. Read `reference/workflow.md`.
2. Read `reference/reference-adaptation.md`.
3. Read `reference/visual-modes.md`.
4. Read `reference/platform-scenarios.md`.
5. If the user asks for example-based visual references, visual examples, informal visual examples or non-professional style references, read `reference/examples-examples-are-not-requirements.md`.
6. If the request includes animation, dynamic background, scroll motion, or React animation, read `reference/animation.md`.
7. Before final handoff for implemented UI, read `reference/verification.md`.
8. If the task changes scope, read `reference/requirement-change-control.md`.
```

- [ ] **Step 3: Add non-negotiable behavior**

Append:

```markdown
## Non-Negotiable Behavior

- Do not start with implementation for broad UI requests.
- First classify the product, platform, audience, and primary job.
- Offer 2-4 design directions when the user has not already chosen a precise direction.
- Include both Dynamic Future Mode and Simple Designed Mode when both are plausible.
- Treat user-provided visual examples as reference clues only unless explicitly confirmed.
- Treat useful external and installed skill references as source material for principles, not as text or templates to copy.
- Rewrite reference ideas into this skill's own workflow, vocabulary, and decision rules.
- Avoid default purple-blue gradients, generic dark tech UI, nested cards, and low-contrast decorative panels.
- Motion must express state, hierarchy, causality, data, or spatial continuity.
- Every motion-heavy direction must include reduced-motion and mobile fallback notes.
```

- [ ] **Step 4: Verify file exists**

Run:

```powershell
Test-Path -LiteralPath 'E:\ui-skill\SKILL.md'
```

Expected: `True`

## Task 2: Create Workflow Reference

**Files:**
- Create: `E:\ui-skill\reference\workflow.md`

- [ ] **Step 1: Create `reference` directory**

Run:

```powershell
New-Item -ItemType Directory -Path 'E:\ui-skill\reference' -Force
```

Expected: directory exists.

- [ ] **Step 2: Write workflow reference**

Create `reference\workflow.md`:

```markdown
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
- Acceptance criteria.
- Open questions.
- Potential conflicts.

## Step 1: Understand

Identify:

- Product type.
- Target user.
- Primary user job.
- Platform.
- Brand/product classification.
- Time horizon: quick browsing, long-use tool, presentation, creation, monitoring, transaction.

## Step 2: Classify

Classify as one:

- Brand surface.
- Product surface.
- Hybrid surface.

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
```

- [ ] **Step 3: Verify workflow reference contains requirement intake and option generation**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\workflow.md' -Pattern 'Requirement Document Intake|Supported V1 input forms|Offer 2-4 options|Execution-ready frontend design steps|Component breakdown'
```

Expected: matching lines for intake, supported input forms, option generation, execution steps, and component breakdown.

## Task 2.1: Create Reference Adaptation Rules

**Files:**
- Create: `E:\ui-skill\reference\reference-adaptation.md`

- [ ] **Step 1: Write reference adaptation rules**

Create:

```markdown
# Reference Adaptation

Use existing useful skills, websites, and design references as learning material, not as copy source.

## Allowed

- Extract principles.
- Compare tradeoffs.
- Translate ideas into the user's own workflow.
- Combine several references into one coherent system.
- Add original rules where references do not cover the user's goal.

## Not Allowed

- Copy distinctive wording.
- Copy complete section structures.
- Copy examples as-is.
- Copy prompts or templates as-is.
- Let one reference dominate the skill's structure.

## Required Synthesis

When a reference is useful, convert it into:

- A decision rule.
- A checklist item.
- A design option criterion.
- A verification rule.
- A platform or motion constraint.

The final skill should sound like a purpose-built frontend design workflow for this user, not a patched collection of borrowed notes.
```

- [ ] **Step 2: Verify originality rules exist**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\reference-adaptation.md' -Pattern 'not as copy source|decision rule|purpose-built frontend design workflow'
```

Expected: matching lines for copying boundary, synthesis, and user-specific workflow.

## Task 3: Create Visual Modes Reference

**Files:**
- Create: `E:\ui-skill\reference\visual-modes.md`

- [ ] **Step 1: Write visual modes**

Create:

```markdown
# Visual Modes

## Dynamic Future Mode

Use for expressive, cinematic, high-motion, future-facing interfaces.

Allowed tools:

- examples-are-not-requirements inspired surfaces.
- Optical depth.
- GSAP timelines.
- ScrollTrigger for storytelling pages.
- Algorithmic backgrounds.
- Data-driven visual atmosphere.

Constraints:

- Use motion for meaning.
- Avoid single example overload.
- Keep text readable.
- Add reduced-motion fallback.
- Add mobile performance fallback.

## Simple Designed Mode

Use for interfaces that should be quiet, efficient, and still designed.

Traits:

- Strong typography.
- Clean information hierarchy.
- Restrained color.
- Few animations.
- One memorable visual element.
- Precise spacing.

This is not a rough version. It is a deliberate low-noise design mode.
```

- [ ] **Step 2: Verify both modes exist**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\visual-modes.md' -Pattern 'Dynamic Future Mode|Simple Designed Mode'
```

Expected: both mode headings are found.

## Task 4: Create Examples Are Not Requirements Reference

**Files:**
- Create: `E:\ui-skill\reference\examples-examples-are-not-requirements.md`

- [ ] **Step 1: Write example-based visual references reference boundary**

Create:

```markdown
# Examples Are Not Requirements Inspiration

Use Examples Are Not Requirements as inspiration only.

Borrow:

- Translucent material.
- Optical depth.
- Soft reflection and refraction.
- Adaptive controls.
- Smooth spatial continuity.
- Content-first layering.

Do not:

- Hard-code a named product or operating system as a required visual style.
- Copy a product-specific visual asset.
- Recreate a product-specific navigation pattern without confirmation.
- Use blur as a generic decoration.
- Make any single visual example dominate every surface.
- Put low-contrast text on transparent panels.

## Web Translation

For web UI, translate the inspiration into:

- Layered panels with readable contrast.
- Subtle backdrop blur where it clarifies hierarchy.
- Edge highlights and shadows used sparingly.
- Motion that connects trigger and result.
- Static or simplified fallback for low-power devices.
```

- [ ] **Step 2: Verify non-copying rule exists**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\examples-examples-are-not-requirements.md' -Pattern 'Do not hard-code examples'
```

Expected: matching lines for prohibited copying.

## Task 5: Create Platform Scenarios Reference

**Files:**
- Create: `E:\ui-skill\reference\platform-scenarios.md`

- [ ] **Step 1: Write V1 platform classifications**

Create:

```markdown
# Platform Scenarios

## Strong V1 Support

- Web landing page.
- Web app.
- SaaS dashboard.
- Admin panel.
- AI tool.
- Creative tool.
- Data visualization page.
- React or Next.js frontend.

## Directional V1 Support

- Mobile app.
- Mini program.
- Desktop software.
- Large screen display.

For directional support, provide product structure, visual direction, and interaction principles. Do not claim complete native platform compliance.

## Classification Questions

- Is this a brand surface or product surface?
- Is the main task browsing, creating, monitoring, buying, learning, or operating?
- Is the user session short or long?
- Is high motion useful or distracting?
- Does the platform need touch-first controls?
```

- [ ] **Step 2: Verify directional support warning exists**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\platform-scenarios.md' -Pattern 'Do not claim complete native platform compliance'
```

Expected: one matching line.

## Task 6: Create Animation Reference

**Files:**
- Create: `E:\ui-skill\reference\animation.md`

- [ ] **Step 1: Write GSAP routing rules**

Create:

```markdown
# Animation

Use GSAP skills for implementation guidance:

- `gsap-core`: basic tweens and simple UI motion.
- `gsap-timeline`: sequenced entrances and transitions.
- `gsap-scrolltrigger`: scroll storytelling and scroll-linked animation.
- `gsap-plugins`: Flip, Draggable, SplitText, ScrambleText, MorphSVG, MotionPath.
- `gsap-utils`: mapping input values to animation values.
- `gsap-react`: React-safe animation lifecycle.
- `gsap-performance`: performance constraints.
- `gsap-frameworks`: Vue, Svelte, and other framework adaptation.

## Motion Rules

- Prefer transform and opacity.
- Avoid animating layout properties unless necessary.
- Do not hide core content until animation fires.
- Use reduced-motion fallback.
- Use mobile fallback for heavy blur, particles, pinning, and scroll-linked effects.
- Motion must communicate hierarchy, state, causality, data, or spatial continuity.
```

- [ ] **Step 2: Verify GSAP skills are referenced**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\animation.md' -Pattern 'gsap-core|gsap-performance|reduced-motion'
```

Expected: matches for GSAP routing and fallback rules.

## Task 7: Create Verification Reference

**Files:**
- Create: `E:\ui-skill\reference\verification.md`

- [ ] **Step 1: Write QA checklist**

Create:

```markdown
# Verification

Before final handoff after implementation, verify:

- Page loads.
- No blank first screen.
- No console errors.
- Main controls respond.
- Text is readable.
- No incoherent overlap.
- No horizontal mobile overflow.
- Motion does not block content.
- Reduced-motion mode is acceptable.
- Dynamic backgrounds do not reduce contrast.
- Performance is acceptable on mobile-sized viewport.

Use `webapp-testing` or the available browser tool for rendered frontend validation.
```

- [ ] **Step 2: Verify checklist exists**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\verification.md' -Pattern 'No blank first screen|Reduced-motion'
```

Expected: checklist items are found.

## Task 8: Create Requirement Change Control Reference

**Files:**
- Create: `E:\ui-skill\reference\requirement-change-control.md`

- [ ] **Step 1: Write change control policy**

Create:

```markdown
# Requirement Change Control

If a requested code change is not covered by the existing requirement documents:

1. Create or append a requirement note under `spec/`.
2. Name it with the relevant feature and date.
3. State the new requirement, source request, affected files, and acceptance criteria.
4. Do not silently expand implementation scope.

If the new requirement conflicts with an earlier requirement:

1. Stop before editing code.
2. Explain the conflict to the user.
3. Name the conflicting requirement files.
4. Ask the user which requirement wins.
5. Proceed only after explicit user confirmation.
```

- [ ] **Step 2: Verify conflict handling rule exists**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\requirement-change-control.md' -Pattern 'Stop before editing code'
```

Expected: one matching line.

## Task 9: Final Review

**Files:**
- Read: `E:\ui-skill\spec\frontend-skill-v1-requirements.md`
- Read: `E:\ui-skill\SKILL.md`
- Read: `E:\ui-skill\reference\*.md`

- [ ] **Step 1: Verify all required files exist**

Run:

```powershell
$files = @(
  'E:\ui-skill\SKILL.md',
  'E:\ui-skill\reference\workflow.md',
  'E:\ui-skill\reference\reference-adaptation.md',
  'E:\ui-skill\reference\visual-modes.md',
  'E:\ui-skill\reference\examples-examples-are-not-requirements.md',
  'E:\ui-skill\reference\platform-scenarios.md',
  'E:\ui-skill\reference\animation.md',
  'E:\ui-skill\reference\verification.md',
  'E:\ui-skill\reference\requirement-change-control.md'
)
$files | ForEach-Object { [PSCustomObject]@{Path=$_; Exists=(Test-Path -LiteralPath $_)} }
```

Expected: every `Exists` value is `True`.

- [ ] **Step 2: Review against V1 requirements**

Confirm:

- Requirement document intake exists.
- Supported V1 input forms exist.
- Word, PDF, image, Figma, and external docs are explicitly out of scope for automatic parsing in V1.
- Reference adaptation and originality rules exist.
- Dynamic Future Mode exists.
- Simple Designed Mode exists.
- Examples are not requirements.
- Option generation is required.
- Execution-ready frontend design steps include page structure, component breakdown, tokens, motion, responsive behavior, implementation order, and verification.
- GSAP and webapp-testing references exist.
- Requirement change control exists.

## Self-Review

- Spec coverage: Every V1 acceptance criterion maps to a task above, including reference adaptation and originality.
- Placeholder scan: No task uses TBD, TODO, or vague later work.
- Type consistency: File names in tasks match the file structure section.
