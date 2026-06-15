# Frontend Skill V1 Examples Layer Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a small `examples/` calibration layer that demonstrates expected routing and output shape for common frontend design requests.

**Architecture:** Add a new `examples/` folder with three Markdown examples. Do not change existing core layers in this pass.

**Tech Stack:** Markdown-only Codex/agent skill files under `E:\ui-skill`.

---

## Files Expected To Change

- Create: `E:\ui-skill\examples\web-product-ai-tool.md`
- Create: `E:\ui-skill\examples\landing-brand-page.md`
- Create: `E:\ui-skill\examples\informal-visual-example.md`

## Task 1: Create Examples Folder

- [ ] **Step 1: Create folder**

Run:

```powershell
New-Item -ItemType Directory -Path 'E:\ui-skill\examples' -Force
```

Expected: `E:\ui-skill\examples` exists.

## Task 2: Write Calibration Examples

- [ ] **Step 1: Create three example files**

Each file must include:

- `## User Request`
- `## Expected Routing`
- `## Expected Requirement Interpretation`
- `## Expected Design Direction Shape`
- `## Expected Output Shape`
- `## Notes On What Not To Do`

Example coverage:

- `web-product-ai-tool.md`: SaaS or AI tool request that routes through `tracks/web-product.md` and may compare both modes.
- `landing-brand-page.md`: brand or landing page request that routes through `tracks/landing-brand.md`.
- `informal-visual-example.md`: user gives non-professional visual examples; must route through `rules/examples-are-not-requirements.md`.

## Task 3: Verify Examples Layer

- [ ] **Step 1: Verify files exist**

Run:

```powershell
Get-ChildItem -LiteralPath 'E:\ui-skill\examples' -File | Select-Object Name,Length
```

Expected: three files exist and are non-empty.

- [ ] **Step 2: Verify required headings**

Run:

```powershell
$required = @('## User Request','## Expected Routing','## Expected Requirement Interpretation','## Expected Design Direction Shape','## Expected Output Shape','## Notes On What Not To Do')
Get-ChildItem -LiteralPath 'E:\ui-skill\examples' -File | Sort-Object Name | ForEach-Object {
  $text = Get-Content -LiteralPath $_.FullName -Raw
  foreach ($h in $required) {
    [PSCustomObject]@{File=$_.Name; Heading=$h; Present=($text -like "*$h*")}
  }
}
```

Expected: every `Present` value is `True`.

- [ ] **Step 3: Verify no core layers changed**

Run:

```powershell
git status --short
```

Expected: only `examples/`, this spec file, and this plan file are new or changed.

## Self-Review

- Scope: Only adds examples and planning/spec records.
- Requirement coverage: Three examples cover web product, landing brand, and informal visual language.
- Risk: Examples must not become mandatory recipes; they should demonstrate routing, not prescribe fixed design outcomes.
