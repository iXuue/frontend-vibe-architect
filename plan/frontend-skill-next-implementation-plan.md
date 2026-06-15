# Frontend Future Design Skill Next Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Extend V1 into a broader frontend design skill with richer requirement document intake, requirement traceability, platform-specific rules, reference-image workflows, design option schemas, stack guidance, and stronger verification.

**Architecture:** Keep `SKILL.md` as the routing entry and add focused reference documents under `reference/`. Do not merge platform rules into one large block if separate files make maintenance easier.

**Tech Stack:** Markdown-based Agent Skill, optional future scripts only if manual checklists become too repetitive.

---

## File Structure

- Modify: `E:\ui-skill\SKILL.md`
  - Add next-version references to reading order after V1 is stable.
- Create: `E:\ui-skill\reference\platform-web.md`
  - Web-specific rules.
- Create: `E:\ui-skill\reference\requirement-document-intake.md`
  - Rich requirement document extraction and conflict detection.
- Create: `E:\ui-skill\reference\requirement-traceability.md`
  - Mapping source requirements to design decisions and execution steps.
- Create: `E:\ui-skill\reference\platform-mobile.md`
  - iOS and Android design-direction rules.
- Create: `E:\ui-skill\reference\platform-mini-program.md`
  - WeChat mini program constraints.
- Create: `E:\ui-skill\reference\platform-desktop.md`
  - Desktop software direction rules.
- Create: `E:\ui-skill\reference\platform-large-screen.md`
  - Large-screen and data visualization rules.
- Create: `E:\ui-skill\reference\reference-image-workflow.md`
  - Reference image decision and conversion workflow.
- Create: `E:\ui-skill\reference\design-option-schema.md`
  - Required option output schema.
- Create: `E:\ui-skill\reference\stack-guidance.md`
  - Implementation stack recommendation rules.
- Modify: `E:\ui-skill\reference\verification.md`
  - Extend QA coverage.

## Task 0: Add Requirement Document Intake

**Files:**
- Create: `E:\ui-skill\reference\requirement-document-intake.md`

- [ ] **Step 1: Write requirement document intake rules**

Create:

```markdown
# Requirement Document Intake

Extract from the user's requirement document:

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

Before design options, output a requirement summary.

If requirements conflict, stop and ask the user which requirement wins.
```

- [ ] **Step 2: Verify conflict handling**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\requirement-document-intake.md' -Pattern 'If requirements conflict'
```

Expected: one matching line.

## Task 0.1: Add Requirement Traceability

**Files:**
- Create: `E:\ui-skill\reference\requirement-traceability.md`

- [ ] **Step 1: Write traceability rules**

Create:

```markdown
# Requirement Traceability

For broad frontend work, keep a simple mapping:

- Source requirement.
- Design decision.
- Implementation step.
- Verification check.

Use this mapping to explain why each major design decision exists.
Do not introduce major UI behavior that cannot be traced to a requirement, a user-approved design direction, or an explicitly stated assumption.
```

- [ ] **Step 2: Verify traceability fields**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\requirement-traceability.md' -Pattern 'Source requirement|Design decision|Implementation step|Verification check'
```

Expected: all fields are found.

## Task 1: Add Platform Web Rules

**Files:**
- Create: `E:\ui-skill\reference\platform-web.md`

- [ ] **Step 1: Write web platform rules**

Create:

```markdown
# Platform: Web

Use for:

- Landing pages.
- Marketing sites.
- Web apps.
- SaaS dashboards.
- Admin panels.
- AI tools.
- Creative tools.

Rules:

- Respect responsive layout.
- Avoid horizontal mobile overflow.
- Keep navigation predictable.
- Keep primary action visible.
- Use animation more freely on brand surfaces than product surfaces.
- For product surfaces, prioritize density, scanning, and repeated use.

Anti-patterns:

- One generic hero for every product.
- Cards for every section.
- Scroll hijacking on task-heavy pages.
- low-contrast decorative panels.
```

- [ ] **Step 2: Verify file**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\platform-web.md' -Pattern 'Landing pages|Scroll hijacking'
```

Expected: matching lines exist.

## Task 2: Add Mobile Rules

**Files:**
- Create: `E:\ui-skill\reference\platform-mobile.md`

- [ ] **Step 1: Write mobile rules**

Create:

```markdown
# Platform: Mobile App

Use for iOS and Android direction.

Rules:

- Touch targets must be large enough.
- Navigation must support thumb reach.
- Avoid dense desktop layouts.
- Respect safe areas.
- Use fewer simultaneous animations than web landing pages.
- Prioritize task clarity over visual atmosphere.

Limits:

- This skill provides design direction unless a native implementation stack is explicitly in scope.
- Do not claim full iOS or Android HIG compliance without platform-specific review.
```

- [ ] **Step 2: Verify platform limitation**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\platform-mobile.md' -Pattern 'Do not claim full iOS or Android HIG compliance'
```

Expected: one matching line.

## Task 3: Add Mini Program Rules

**Files:**
- Create: `E:\ui-skill\reference\platform-mini-program.md`

- [ ] **Step 1: Write mini program rules**

Create:

```markdown
# Platform: Mini Program

Use for WeChat mini program design direction.

Rules:

- Keep flows short.
- Prioritize fast task completion.
- Avoid heavy animation.
- Use familiar navigation patterns.
- Keep content readable on small screens.
- Avoid desktop-style dashboards.

Limits:

- V1/Next design direction must be checked against the target mini program framework before implementation.
```

- [ ] **Step 2: Verify rules**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\platform-mini-program.md' -Pattern 'Keep flows short|Avoid heavy animation'
```

Expected: matching lines exist.

## Task 4: Add Desktop Rules

**Files:**
- Create: `E:\ui-skill\reference\platform-desktop.md`

- [ ] **Step 1: Write desktop rules**

Create:

```markdown
# Platform: Desktop Software

Use for desktop app direction.

Rules:

- Support dense but organized information.
- Use toolbars, panels, inspectors, sidebars, and command surfaces where appropriate.
- Keep window resizing in mind.
- Avoid marketing-page hero layouts inside tools.
- Use keyboard affordances where relevant.
- Motion should clarify state, not decorate.

Limits:

- Match native platform conventions when a specific platform is named.
```

- [ ] **Step 2: Verify desktop anti-pattern**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\platform-desktop.md' -Pattern 'Avoid marketing-page hero layouts'
```

Expected: one matching line.

## Task 5: Add Large-Screen Rules

**Files:**
- Create: `E:\ui-skill\reference\platform-large-screen.md`

- [ ] **Step 1: Write large-screen rules**

Create:

```markdown
# Platform: Large Screen

Use for data walls, monitoring displays, and presentation dashboards.

Rules:

- Prioritize at-a-glance comprehension.
- Use strong hierarchy.
- Avoid tiny text.
- Use motion to show live state, not decoration.
- Keep contrast high.
- Provide static fallback for heavy generated visuals.

Risks:

- Large screens can make weak hierarchy look worse.
- Too much animation reduces readability.
```

- [ ] **Step 2: Verify live-state rule**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\platform-large-screen.md' -Pattern 'live state'
```

Expected: one matching line.

## Task 6: Add Reference Image Workflow

**Files:**
- Create: `E:\ui-skill\reference\reference-image-workflow.md`

- [ ] **Step 1: Write reference image workflow**

Create:

```markdown
# Reference Image Workflow

Use reference images when:

- The visual direction is ambiguous.
- The user asks for future, premium, cinematic, example-based, future, premium, cinematic, or highly dynamic UI.
- The page is brand-heavy.
- Multiple visual directions need comparison.

Do not use reference images when:

- The task is a small UI fix.
- The existing design system already decides the visual language.

Workflow:

1. Write 2-4 visual directions.
2. For each direction, write a reference-image prompt.
3. Ask the user which direction to explore if generation is costly.
4. Convert chosen reference into tokens, layout, components, and motion.
5. Do not copy image text or impossible layout literally.
```

- [ ] **Step 2: Verify conversion rule**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\reference-image-workflow.md' -Pattern 'Convert chosen reference'
```

Expected: one matching line.

## Task 7: Add Design Option Schema

**Files:**
- Create: `E:\ui-skill\reference\design-option-schema.md`

- [ ] **Step 1: Write option schema**

Create:

```markdown
# Design Option Schema

Every broad design option must include:

- Option name.
- Best fit.
- Product assumption.
- User job.
- Visual signature.
- Layout model.
- Material model.
- Typography model.
- Motion model.
- Reference-image direction.
- Implementation stack.
- Complexity rating: low, medium, or high.
- Maintenance risk.
- Accessibility risk.
- Performance risk.
```

- [ ] **Step 2: Verify risk fields**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\design-option-schema.md' -Pattern 'Accessibility risk|Performance risk'
```

Expected: matching lines exist.

## Task 8: Add Stack Guidance

**Files:**
- Create: `E:\ui-skill\reference\stack-guidance.md`

- [ ] **Step 1: Write stack guidance**

Create:

```markdown
# Stack Guidance

Recommend:

- Static HTML/CSS for small static pages.
- React + Vite for complex interactive web apps.
- Next.js for routed production web apps, SSR, content, and deployment workflows.
- GSAP for advanced web animation.
- Three.js only when real 3D is necessary.
- Existing project stack when modifying an existing app.

Do not add dependencies only for visual novelty.
```

- [ ] **Step 2: Verify dependency rule**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\stack-guidance.md' -Pattern 'Do not add dependencies'
```

Expected: one matching line.

## Task 9: Extend Verification

**Files:**
- Modify: `E:\ui-skill\reference\verification.md`

- [ ] **Step 1: Add extended QA section**

Append:

```markdown

## Extended QA

Check:

- Desktop viewport.
- Mobile viewport.
- Reduced motion.
- Low-performance fallback.
- Text overflow.
- Contrast.
- Keyboard navigation.
- Console errors.
- Dynamic effect non-blank rendering.
- Touch target size for mobile-like surfaces.
```

- [ ] **Step 2: Verify extended QA**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\verification.md' -Pattern 'Dynamic effect non-blank rendering|Touch target size'
```

Expected: matching lines exist.

## Self-Review

- Spec coverage: Every next-version requirement maps to a task.
- Placeholder scan: No placeholders are present.
- Type consistency: File names are consistent across task list and file structure.
