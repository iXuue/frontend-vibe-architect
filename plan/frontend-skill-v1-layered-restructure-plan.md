# Frontend Skill V1 Layered Restructure Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Restructure the V1 frontend design skill from a flat reference collection into a layered, callable skill with entry, flow, track, mode, rule, and output-template layers.

**Architecture:** `SKILL.md` becomes a compact router. Detailed behavior moves into focused folders: `flows/` for process, `tracks/` for product/platform paths, `modes/` for visual modes, `rules/` for constraints, and `output/` for stable response templates. Existing `reference/` files are migrated into the new layer structure, then the old `reference/` folder is left unused unless the user later approves deletion.

**Tech Stack:** Markdown-based Codex/agent skill under `E:\ui-skill`; no runtime dependencies; no scripts required for V1.

---

## File Structure

- Modify: `E:\ui-skill\SKILL.md`
  - Compact entry point, routing logic, mandatory sequence, and layer reading rules.
- Create: `E:\ui-skill\flows\intake.md`
  - Requirement document intake and requirement summary process.
- Create: `E:\ui-skill\flows\choose-track.md`
  - Rules for choosing product/platform track files.
- Create: `E:\ui-skill\flows\design-options.md`
  - 2-4 design option generation process.
- Create: `E:\ui-skill\flows\execution-steps.md`
  - Conversion from selected option to execution-ready frontend steps.
- Create: `E:\ui-skill\flows\handoff.md`
  - Final response and implementation handoff rules.
- Create: `E:\ui-skill\tracks\web-product.md`
  - Web app, SaaS, dashboard, admin, AI tool, and creative tool direction.
- Create: `E:\ui-skill\tracks\landing-brand.md`
  - Website, landing page, brand, and launch surface direction.
- Create: `E:\ui-skill\tracks\mobile-direction.md`
  - Mobile app and mini program design direction boundaries.
- Create: `E:\ui-skill\tracks\desktop-direction.md`
  - Desktop software design direction.
- Create: `E:\ui-skill\tracks\data-visualization.md`
  - Dashboard, monitoring page, and large-screen data display direction.
- Create: `E:\ui-skill\modes\dynamic-future.md`
  - Dynamic Future Mode.
- Create: `E:\ui-skill\modes\simple-designed.md`
  - Simple Designed Mode.
- Create: `E:\ui-skill\rules\reference-adaptation.md`
  - Reference learning and originality rules.
- Create: `E:\ui-skill\rules\examples-examples-are-not-requirements.md`
  - examples-are-not-requirements rule.
- Create: `E:\ui-skill\rules\animation.md`
  - GSAP and motion rules.
- Create: `E:\ui-skill\rules\verification.md`
  - QA and validation rules.
- Create: `E:\ui-skill\rules\requirement-change-control.md`
  - Requirement drift and conflict policy.
- Create: `E:\ui-skill\output\requirement-summary.md`
  - Requirement summary response template.
- Create: `E:\ui-skill\output\design-options.md`
  - Design options response template.
- Create: `E:\ui-skill\output\design-brief.md`
  - Chosen direction brief template.
- Create: `E:\ui-skill\output\frontend-execution-plan.md`
  - Execution-ready frontend design steps template.

## Task 1: Rewrite Main Skill Router

**Files:**
- Modify: `E:\ui-skill\SKILL.md`

- [ ] **Step 1: Backup existing file**

Run:

```powershell
$ts = Get-Date -Format 'yyyyMMdd-HHmmss'
$backup = "E:\codex_backup\$ts-rewrite-layered-skill"
New-Item -ItemType Directory -Path $backup -Force | Out-Null
Copy-Item -LiteralPath 'E:\ui-skill\SKILL.md' -Destination (Join-Path $backup 'SKILL.md') -Force
Write-Output $backup
```

Expected: backup directory path is printed.

- [ ] **Step 2: Replace `SKILL.md` with router content**

Write `E:\ui-skill\SKILL.md` with:

```markdown
---
name: frontend-future-design
description: Use when the user wants an agent to read frontend requirements, design product-appropriate UI options, and produce execution-ready frontend design steps for websites, web apps, dashboards, AI tools, mobile directions, mini program directions, desktop software directions, or data visualization surfaces.
---

# Frontend Future Design

This skill reads a user's requirement document, classifies the frontend product surface, proposes design directions, and converts the selected direction into execution-ready frontend design steps.

## Layered Reading Order

1. Read `flows/intake.md`.
2. Read `flows/choose-track.md`.
3. Read the selected file from `tracks/`.
4. Read `rules/reference-adaptation.md`.
5. Read the relevant files from `modes/`.
6. Read any relevant files from `rules/`.
7. Use the required template from `output/`.

## Mandatory Sequence

1. Intake the requirement.
2. Output a requirement summary.
3. Choose one primary track and optional secondary track.
4. Choose one or more visual modes.
5. Generate 2-4 design options when direction is not already precise.
6. Ask for user direction when scope is broad, high-impact, or visually ambiguous.
7. Produce a design brief after the direction is confirmed or low-risk recommendation is justified.
8. Produce execution-ready frontend design steps.
9. Verify against `rules/verification.md` before final handoff for implemented UI.

## Hard Rules

- Do not copy reference skills, websites, wording, examples, prompts, or templates directly.
- Treat user-provided visual examples as reference clues only unless explicitly confirmed.
- Do not force Dynamic Future Mode onto dense operational tools where clarity matters more.
- Do not start implementation for broad UI work before requirement summary, track choice, mode choice, and direction choice are clear.
- If a requested code change is not covered by `spec/`, follow `rules/requirement-change-control.md`.
```

- [ ] **Step 3: Verify router behavior**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\SKILL.md' -Pattern 'Layered Reading Order|Mandatory Sequence|flows/intake.md|tracks/|output/|Hard Rules'
```

Expected: matching lines for the router sections and layer references.

## Task 2: Create Flow Layer

**Files:**
- Create: `E:\ui-skill\flows\intake.md`
- Create: `E:\ui-skill\flows\choose-track.md`
- Create: `E:\ui-skill\flows\design-options.md`
- Create: `E:\ui-skill\flows\execution-steps.md`
- Create: `E:\ui-skill\flows\handoff.md`

- [ ] **Step 1: Create folder**

Run:

```powershell
New-Item -ItemType Directory -Path 'E:\ui-skill\flows' -Force
```

Expected: `E:\ui-skill\flows` exists.

- [ ] **Step 2: Write `intake.md`**

Create:

```markdown
# Flow: Requirement Intake

Supported V1 input forms:

- Plain text pasted by the user.
- Markdown requirement documents.
- Local `.md` or `.txt` files when the user provides an explicit path.
- Short user messages that can be normalized into a lightweight requirement document.

V1 does not promise automatic parsing of Word documents, PDFs, images, Figma files, or external product docs unless a later requirement explicitly adds that capability.

Extract:

- Product goal.
- Target users.
- Target platforms.
- Required pages or screens.
- Core workflows.
- Content constraints.
- Visual constraints.
- Technical constraints.
- Accessibility constraints.
- Acceptance criteria.
- Open questions.
- Potential conflicts.

Before design work, produce a requirement summary using `output/requirement-summary.md`.

If a material requirement is unclear and affects scope, platform, architecture, or acceptance criteria, ask the user before proceeding.
```

- [ ] **Step 3: Write `choose-track.md`**

Create:

```markdown
# Flow: Choose Track

Choose one primary track and optional secondary track.

Primary tracks:

- `tracks/web-product.md`: web apps, SaaS tools, dashboards, admin panels, AI tools, creative tools.
- `tracks/landing-brand.md`: websites, landing pages, launch pages, brand surfaces.
- `tracks/mobile-direction.md`: mobile app and mini program direction.
- `tracks/desktop-direction.md`: desktop software direction.
- `tracks/data-visualization.md`: data dashboards, monitoring, large-screen displays.

Choose by answering:

- Is the surface brand-led, product-led, or hybrid?
- Is the main job browsing, creating, monitoring, operating, buying, learning, or presenting?
- Is the session short or repeated?
- Does the platform need touch, keyboard, dense tables, or large-screen viewing?
- Would heavy motion help understanding or distract from work?

State the chosen track before generating design options.
```

- [ ] **Step 4: Write `design-options.md`**

Create:

```markdown
# Flow: Design Options

Generate 2-4 options when the user has not already chosen a precise direction.

Each option must include:

- Name.
- Best-fit scenario.
- Track.
- Visual mode.
- Visual language.
- Layout strategy.
- Color and material strategy.
- Motion strategy.
- Reference-image direction.
- Implementation difficulty.
- Risks.

Include both Dynamic Future Mode and Simple Designed Mode when both are plausible.

For broad, high-impact, or visually ambiguous work, ask the user to choose, combine, or reject options before implementation.
```

- [ ] **Step 5: Write `execution-steps.md`**

Create:

```markdown
# Flow: Execution Steps

After direction confirmation or low-risk recommendation, convert the chosen direction into execution-ready frontend design steps.

The execution steps must include:

- Page or screen structure.
- Component breakdown.
- Visual token guidance.
- Motion and interaction rules.
- Responsive behavior rules.
- Recommended implementation order.
- Verification steps.

Use `output/frontend-execution-plan.md`.
```

- [ ] **Step 6: Write `handoff.md`**

Create:

```markdown
# Flow: Handoff

For design-only work, hand off:

- Requirement summary.
- Chosen track and visual mode.
- Design options or chosen design brief.
- Risks and assumptions.

For implementation-ready work, also hand off:

- Execution-ready frontend design steps.
- Verification checklist.
- Required browser or visual QA.

If implementation has already happened, verify with `rules/verification.md` before final response.
```

- [ ] **Step 7: Verify flow layer**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\flows\intake.md','E:\ui-skill\flows\choose-track.md','E:\ui-skill\flows\design-options.md','E:\ui-skill\flows\execution-steps.md','E:\ui-skill\flows\handoff.md' -Pattern 'Requirement Intake|Choose Track|Design Options|Execution Steps|Handoff'
```

Expected: every flow file has its matching heading.

## Task 3: Create Track Layer

**Files:**
- Create: `E:\ui-skill\tracks\web-product.md`
- Create: `E:\ui-skill\tracks\landing-brand.md`
- Create: `E:\ui-skill\tracks\mobile-direction.md`
- Create: `E:\ui-skill\tracks\desktop-direction.md`
- Create: `E:\ui-skill\tracks\data-visualization.md`

- [ ] **Step 1: Create folder**

Run:

```powershell
New-Item -ItemType Directory -Path 'E:\ui-skill\tracks' -Force
```

Expected: `E:\ui-skill\tracks` exists.

- [ ] **Step 2: Create track files**

Write the five files with focused guidance:

`web-product.md`:

```markdown
# Track: Web Product

Use for web apps, SaaS tools, dashboards, admin panels, AI tools, and creative tools.

Prioritize:

- Clear navigation.
- Repeated-use efficiency.
- Stable controls.
- Empty, loading, error, and success states.
- Dense but readable information hierarchy.
- Keyboard and responsive behavior when relevant.

Avoid marketing-page composition for operational workflows.
```

`landing-brand.md`:

```markdown
# Track: Landing Brand

Use for websites, launch pages, brand pages, and product storytelling surfaces.

Prioritize:

- First-viewport product or offer signal.
- Strong visual signature.
- Clear narrative sections.
- Mobile-first readability.
- Calls to action with clear hierarchy.
- Reference images when visual ambiguity is high.

Avoid generic SaaS hero layouts and decorative sections that do not explain the product.
```

`mobile-direction.md`:

```markdown
# Track: Mobile Direction

Use for mobile app and mini program design direction.

V1 provides direction, not full native platform compliance.

Prioritize:

- Touch-first controls.
- Short flows.
- Safe area awareness.
- Clear primary action.
- Lower animation budget.
- Fast loading and simple navigation for mini programs.

Do not claim full iOS, Android, or mini program guideline compliance without platform-specific review.
```

`desktop-direction.md`:

```markdown
# Track: Desktop Direction

Use for desktop software design direction.

Prioritize:

- Resizable layouts.
- Persistent navigation or toolbars.
- Keyboard-friendly workflows.
- Higher density.
- Clear panels and inspectors.
- Multi-window or document-like mental models when relevant.

Avoid landing-page hero patterns inside software workspaces.
```

`data-visualization.md`:

```markdown
# Track: Data Visualization

Use for dashboards, monitoring, analytics, and large-screen data displays.

Prioritize:

- Glanceable hierarchy.
- Live state clarity.
- Strong contrast.
- Chart readability.
- Alert and anomaly states.
- Motion only when it clarifies change, flow, or causality.

Avoid decorative data effects that reduce legibility.
```

- [ ] **Step 3: Verify track layer**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\tracks\web-product.md','E:\ui-skill\tracks\landing-brand.md','E:\ui-skill\tracks\mobile-direction.md','E:\ui-skill\tracks\desktop-direction.md','E:\ui-skill\tracks\data-visualization.md' -Pattern '^# Track:'
```

Expected: five matching track headings.

## Task 4: Create Mode Layer

**Files:**
- Create: `E:\ui-skill\modes\dynamic-future.md`
- Create: `E:\ui-skill\modes\simple-designed.md`

- [ ] **Step 1: Create folder**

Run:

```powershell
New-Item -ItemType Directory -Path 'E:\ui-skill\modes' -Force
```

Expected: `E:\ui-skill\modes` exists.

- [ ] **Step 2: Write mode files**

`dynamic-future.md`:

```markdown
# Mode: Dynamic Future

Use when expression, brand memory, spatial storytelling, or dynamic data atmosphere improves the product.

Can use:

- examples-are-not-requirements-inspired surfaces.
- Optical depth.
- Generative or data-driven backgrounds.
- GSAP timelines.
- Scroll-linked storytelling.
- High-quality hover, focus, and state transitions.

Must include:

- Reduced-motion fallback.
- Mobile performance fallback.
- Readable text over all dynamic layers.
- Motion tied to hierarchy, state, causality, data, or spatial continuity.
```

`simple-designed.md`:

```markdown
# Mode: Simple Designed

Use when speed, clarity, repetition, density, accessibility, or operational confidence matters more than visual spectacle.

Use:

- Strong typography.
- Clear hierarchy.
- Precise spacing.
- Restrained color.
- Few animations.
- One memorable visual element.
- Stable layout.

This is a deliberate low-noise design direction, not an unfinished version.
```

- [ ] **Step 3: Verify mode layer**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\modes\dynamic-future.md','E:\ui-skill\modes\simple-designed.md' -Pattern '^# Mode:'
```

Expected: two matching mode headings.

## Task 5: Create Rule Layer

**Files:**
- Create: `E:\ui-skill\rules\reference-adaptation.md`
- Create: `E:\ui-skill\rules\examples-examples-are-not-requirements.md`
- Create: `E:\ui-skill\rules\animation.md`
- Create: `E:\ui-skill\rules\verification.md`
- Create: `E:\ui-skill\rules\requirement-change-control.md`

- [ ] **Step 1: Create folder**

Run:

```powershell
New-Item -ItemType Directory -Path 'E:\ui-skill\rules' -Force
```

Expected: `E:\ui-skill\rules` exists.

- [ ] **Step 2: Migrate rule content**

Use the existing content from:

- `E:\ui-skill\reference\reference-adaptation.md`
- `E:\ui-skill\reference\examples-examples-are-not-requirements.md`
- `E:\ui-skill\reference\animation.md`
- `E:\ui-skill\reference\verification.md`
- `E:\ui-skill\reference\requirement-change-control.md`

Rewrite or move the content into the matching `rules\*.md` files. Keep the same requirements, but make headings use `# Rule: ...`.

- [ ] **Step 3: Verify rule layer**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\rules\reference-adaptation.md','E:\ui-skill\rules\examples-examples-are-not-requirements.md','E:\ui-skill\rules\animation.md','E:\ui-skill\rules\verification.md','E:\ui-skill\rules\requirement-change-control.md' -Pattern '^# Rule:|not as copy source|Do not hard-code examples|gsap-core|No blank first screen|Stop before editing code'
```

Expected: matching lines across the five rule files.

## Task 6: Create Output Template Layer

**Files:**
- Create: `E:\ui-skill\output\requirement-summary.md`
- Create: `E:\ui-skill\output\design-options.md`
- Create: `E:\ui-skill\output\design-brief.md`
- Create: `E:\ui-skill\output\frontend-execution-plan.md`

- [ ] **Step 1: Create folder**

Run:

```powershell
New-Item -ItemType Directory -Path 'E:\ui-skill\output' -Force
```

Expected: `E:\ui-skill\output` exists.

- [ ] **Step 2: Write output templates**

Create `requirement-summary.md`:

```markdown
# Output: Requirement Summary

Use this shape:

- Product goal:
- Target users:
- Target platform:
- Required pages or screens:
- Core workflows:
- Constraints:
- Acceptance criteria:
- Open questions:
- Potential conflicts:
- Assumptions:
```

Create `design-options.md`:

```markdown
# Output: Design Options

For each option:

- Name:
- Best-fit scenario:
- Track:
- Visual mode:
- Visual language:
- Layout strategy:
- Color and material strategy:
- Motion strategy:
- Reference image direction:
- Implementation difficulty:
- Risks:
- Why this fits the requirement:
```

Create `design-brief.md`:

```markdown
# Output: Design Brief

Use after direction confirmation or low-risk recommendation:

- Chosen direction:
- Product rationale:
- Target platform:
- Visual mode:
- Information architecture:
- Component language:
- Design tokens:
- Motion rules:
- Responsive rules:
- Risks:
- User confirmations:
```

Create `frontend-execution-plan.md`:

```markdown
# Output: Frontend Execution Plan

Execution-ready frontend design steps must include:

- Page or screen structure:
- Component breakdown:
- Visual token guidance:
- Motion and interaction rules:
- Responsive behavior rules:
- Recommended implementation order:
- Verification steps:
```

- [ ] **Step 3: Verify output templates**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\output\requirement-summary.md','E:\ui-skill\output\design-options.md','E:\ui-skill\output\design-brief.md','E:\ui-skill\output\frontend-execution-plan.md' -Pattern '^# Output:|Component breakdown|Why this fits the requirement'
```

Expected: output template headings and required execution fields are present.

## Task 7: Final Layer Verification

**Files:**
- Read: `E:\ui-skill\SKILL.md`
- Read: `E:\ui-skill\flows\*.md`
- Read: `E:\ui-skill\tracks\*.md`
- Read: `E:\ui-skill\modes\*.md`
- Read: `E:\ui-skill\rules\*.md`
- Read: `E:\ui-skill\output\*.md`

- [ ] **Step 1: Verify required folders and file counts**

Run:

```powershell
$checks = @(
  @{Path='E:\ui-skill\flows'; Count=5},
  @{Path='E:\ui-skill\tracks'; Count=5},
  @{Path='E:\ui-skill\modes'; Count=2},
  @{Path='E:\ui-skill\rules'; Count=5},
  @{Path='E:\ui-skill\output'; Count=4}
)
$checks | ForEach-Object {
  $actual = (Get-ChildItem -LiteralPath $_.Path -File).Count
  [PSCustomObject]@{Path=$_.Path; Expected=$_.Count; Actual=$actual; Pass=($actual -eq $_.Count)}
}
```

Expected: every `Pass` value is `True`.

- [ ] **Step 2: Verify no unresolved placeholders**

Run:

```powershell
Select-String -Path 'E:\ui-skill\SKILL.md','E:\ui-skill\flows\*.md','E:\ui-skill\tracks\*.md','E:\ui-skill\modes\*.md','E:\ui-skill\rules\*.md','E:\ui-skill\output\*.md' -Pattern 'TBD|TODO|fill in|implement later'
```

Expected: no output.

- [ ] **Step 3: Verify old reference folder is not required by `SKILL.md`**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\SKILL.md' -Pattern 'reference/'
```

Expected: no output.

## Self-Review

- Spec coverage: The layered structure requirement maps to Tasks 1-7.
- Prior requirements preserved: requirement intake, reference adaptation, example-based visual references inspiration boundary, dynamic/simple modes, animation, verification, execution steps, and change control remain covered.
- Deletion safety: This plan does not delete the old `reference/` folder. Deletion requires separate explicit user confirmation.
- Placeholder scan: No planned file content contains TBD, TODO, fill-in, or implement-later placeholders.
