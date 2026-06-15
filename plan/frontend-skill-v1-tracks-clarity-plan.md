# Frontend Skill V1 Tracks Clarity Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite `tracks/` Markdown files so each frontend type has clear use conditions, design priorities, defaults, risks, and output notes.

**Architecture:** Keep the current layered skill structure. This pass edits only `tracks/*.md`; other layers stay unchanged.

**Tech Stack:** Markdown-only Codex/agent skill files under `E:\ui-skill`.

---

## Files Expected To Change

- Modify: `E:\ui-skill\tracks\web-product.md`
- Modify: `E:\ui-skill\tracks\landing-brand.md`
- Modify: `E:\ui-skill\tracks\mobile-direction.md`
- Modify: `E:\ui-skill\tracks\desktop-direction.md`
- Modify: `E:\ui-skill\tracks\data-visualization.md`

## Task 1: Backup Existing Track Files

- [ ] **Step 1: Create backup**

Run:

```powershell
$ts = Get-Date -Format 'yyyyMMdd-HHmmss'
$backup = "E:\codex_backup\$ts-tracks-clarity-pass"
New-Item -ItemType Directory -Path $backup -Force | Out-Null
Copy-Item -LiteralPath 'E:\ui-skill\tracks' -Destination (Join-Path $backup 'tracks') -Recurse -Force
Write-Output $backup
```

Expected: backup directory path is printed.

## Task 2: Rewrite Track Files

- [ ] **Step 1: Rewrite all `tracks/*.md` files**

Each file must include:

- `## Use When`
- `## Primary Goal`
- `## Design Priorities`
- `## Layout Defaults`
- `## Interaction Defaults`
- `## Visual Risk`
- `## Do`
- `## Do Not`
- `## Output Notes`

The content must preserve the current five tracks:

- Web Product.
- Landing Brand.
- Mobile Direction.
- Desktop Direction.
- Data Visualization.

## Task 3: Verify Track Layer

- [ ] **Step 1: Verify required headings**

Run:

```powershell
$required = @('## Use When','## Primary Goal','## Design Priorities','## Layout Defaults','## Interaction Defaults','## Visual Risk','## Do','## Do Not','## Output Notes')
Get-ChildItem -LiteralPath 'E:\ui-skill\tracks' -File | Sort-Object Name | ForEach-Object {
  $text = Get-Content -LiteralPath $_.FullName -Raw
  foreach ($h in $required) {
    [PSCustomObject]@{File=$_.Name; Heading=$h; Present=($text -like "*$h*")}
  }
}
```

Expected: every `Present` value is `True`.

- [ ] **Step 2: Verify no out-of-scope files changed by this pass**

Run:

```powershell
Get-ChildItem -LiteralPath 'E:\ui-skill\flows','E:\ui-skill\modes','E:\ui-skill\rules','E:\ui-skill\output' -File | Select-Object FullName,LastWriteTime
```

Expected: these files are not modified during this pass.

## Self-Review

- Scope: Only `tracks/` is edited.
- Requirement coverage: The tracks clarity requirement maps to Tasks 2-3.
- Risk: The main risk is making track files too long; keep them practical and decision-oriented.
