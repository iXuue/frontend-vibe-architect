---
name: frontend-future-design
description: Use when the user wants an agent to read frontend requirements, separate hard requirements from reference examples, choose the right frontend track, generate product-appropriate UI design options, and produce execution-ready frontend implementation steps.
---

# Frontend Future Design

This skill is a requirement-driven frontend design router.

It reads a user's requirement document or lightweight request, classifies the frontend surface, chooses the right design track and visual mode, applies safety rules, and produces stable frontend design outputs.

## Required Workflow

Always follow this order for substantial frontend work:

1. Read `flows/intake.md`.
2. Produce a requirement summary with `output/requirement-summary.md`.
3. Read `flows/choose-track.md`.
4. Choose one primary track and optional secondary track.
5. Read the selected track file from `tracks/`.
6. Read `strategy/README.md`.
7. Choose one primary strategy and optional secondary strategy.
8. Read the selected strategy file from `strategy/`.
9. Read `rules/reference-adaptation.md`.
10. Read `rules/examples-are-not-requirements.md`.
11. Choose one or more mode files from `modes/`.
12. Read any additional rule files needed by the request.
13. Generate design options with `flows/design-options.md` and `output/design-options.md`.
14. Ask for user direction when required.
15. Produce a design brief with `output/design-brief.md` after direction confirmation or low-risk recommendation.
16. Produce execution-ready frontend steps with `flows/execution-steps.md` and `output/frontend-execution-plan.md` when implementation planning is requested.
17. Use `flows/handoff.md` before final response.

## Routing Table

Use these routing rules as pseudo-code. Read the matching files; do not treat this table as a replacement for the detailed layer files.

### Intake Routing

```text
IF request is frontend design, redesign, critique, planning, or implementation:
  READ flows/intake.md
  OUTPUT output/requirement-summary.md

IF request includes a local .md or .txt requirement path:
  READ the file content first
  THEN READ flows/intake.md

IF request is broad, high-impact, or visually ambiguous:
  DO NOT implement before requirement summary, track choice, mode choice, and direction choice are clear
```

### Track Routing

```text
IF request is SaaS, web app, admin, dashboard, AI tool, creative tool, or workspace:
  READ tracks/web-product.md

IF request is website, landing page, launch page, campaign, portfolio, or brand storytelling:
  READ tracks/landing-brand.md

IF request is mobile app, mobile web direction, or mini program:
  READ tracks/mobile-direction.md

IF request is desktop software, professional tool, editor, control panel, or document-like app:
  READ tracks/desktop-direction.md

IF request is analytics, monitoring, metrics, reporting, large-screen display, or chart-heavy UI:
  READ tracks/data-visualization.md

IF request fits more than one track:
  CHOOSE one primary track
  CHOOSE optional secondary track
  STATE why
```

### Strategy Routing

```text
AFTER track choice:
  READ strategy/README.md
  CHOOSE one primary strategy
  CHOOSE optional secondary strategy only when product requirements justify it
  READ the selected strategy file or files
  STATE why

IF product needs repeated task speed, workflow efficiency, density, or low friction:
  READ strategy/efficiency-first.md

IF product needs trust, safety, confidence, sensitive decisions, or serious professional use:
  READ strategy/trust-first.md

IF product needs signup, purchase, booking, trial, lead generation, or offer persuasion:
  READ strategy/conversion-first.md

IF product needs browsing, discovery, search, filtering, comparison, or optional paths:
  READ strategy/exploration-first.md

IF product needs brand personality, creativity, memorability, or emotional impression:
  READ strategy/expression-first.md

IF product needs monitoring, analytics, metrics, reporting, comparison, or decisions from data:
  READ strategy/data-insight-first.md

IF product needs atmosphere, narrative, spatial feeling, immersive presentation, or high-impact scenes:
  READ strategy/immersive-first.md
```

### Mode Routing

```text
IF product needs memorability, atmosphere, advanced interaction, spatial storytelling, or dynamic data feeling:
  CONSIDER modes/dynamic-future.md

IF product needs clarity, repeated use, density, accessibility, operational confidence, or low visual fatigue:
  CONSIDER modes/simple-designed.md

IF both modes are plausible:
  OFFER both as design options

IF user only gives a visual example:
  DO NOT choose a mode solely from the example
  READ rules/examples-are-not-requirements.md
```

### Rule Routing

```text
IF using external skills, websites, screenshots, notes, or design references:
  READ rules/reference-adaptation.md

IF user gives non-professional visual language, style examples, named products, trends, materials, or vague aesthetic terms:
  READ rules/style-fit-from-requirements.md
  READ rules/examples-are-not-requirements.md

IF request involves animation, dynamic background, scroll motion, micro-interactions, GSAP, or motion-heavy UI:
  READ rules/animation.md

IF implementation exists or final handoff needs quality claims:
  READ rules/verification.md

IF user asks for a code or skill behavior change not covered by spec/:
  READ rules/requirement-change-control.md
```

### Output Routing

```text
IF intake is complete:
  USE output/requirement-summary.md

IF design directions are needed:
  USE output/design-options.md

IF a direction is confirmed or low-risk recommendation is justified:
  USE output/design-brief.md

IF frontend implementation planning is requested:
  USE output/frontend-execution-plan.md
```

### Language Routing

```text
IF request includes vague, subjective, example-based, or non-professional design language:
  FIRST complete output/requirement-summary.md
  THEN choose track through flows/choose-track.md
  THEN choose strategy through strategy/README.md
  THEN READ rules/style-fit-from-requirements.md
  THEN READ relevant language/
  THEN generate design options or ask required clarification questions

IF user design language conflicts with product-fit strategy:
  EXPLAIN the conflict
  OFFER options or ask the user to choose
```

### Example Routing

```text
IF agent is unsure how a common request should move through the skill:
  OPTIONALLY READ examples/
  USE examples only for calibration of routing and output shape
  DO NOT copy examples as fixed templates, wording, layouts, or visual recipes

IF examples conflict with user requirements:
  FOLLOW user requirements after applying requirement summary and rule gates
```

### Deprecated Reference Routing

```text
IF considering reference/:
  TREAT reference/ as deprecated historical context
  DO NOT use reference/ as the active skill path
  ONLY READ reference/ when explicitly needed for old-draft comparison
```

### Eval Routing

```text
IF modifying this skill's routing, flows, tracks, modes, rules, outputs, examples, or maintenance docs:
  READ relevant evals/
  CHECK expected routing, stop conditions, output templates, and forbidden behavior

IF using this skill for normal frontend design work:
  DO NOT read evals/ by default
```

## Stop Conditions

Stop and ask the user before proceeding when:

- Product goal is unclear.
- Target platform would materially change the design.
- Required screens or workflows are missing.
- Requirements conflict.
- User examples may be mistaken for hard requirements.
- Broad or high-impact UI work has no chosen direction.
- Implementation is requested before design direction is confirmed.
- A requested code or skill behavior change is not covered by `spec/`.
- Verification requires running a local app but no run command or target is known.

## Hard Rules

- Do not copy reference skills, websites, wording, examples, prompts, or templates directly.
- Do not turn a user-provided visual example into a fixed requirement unless the user explicitly confirms it.
- Do not copy `examples/` as output templates or fixed design recipes.
- Do not read deprecated `reference/` as the active skill path.
- Do not use `evals/` as normal design templates or final answer examples.
- Use `evals/` only for skill maintenance or behavior regression checks.
- Do not choose style from user adjectives before reading requirements and choosing a product track.
- Do not let `language/` override product-fit reasoning from `rules/style-fit-from-requirements.md`.
- Do not force `modes/dynamic-future.md` onto dense operational tools where clarity matters more.
- Do not start implementation for broad UI work before requirement summary, track choice, mode choice, and direction choice are clear.
- Do not claim verification, accessibility, responsiveness, or rendered UI quality unless checked or explicitly marked as unverified.
- If a requested code change is not covered by `spec/`, follow `rules/requirement-change-control.md`.
