# Frontend Skill V1 Modes Clarity Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite `modes/` Markdown files so each visual mode has clear use conditions, design intent, variables, safeguards, and output notes.

**Architecture:** Keep the current layered skill structure. This pass edits only `modes/*.md`; other layers stay unchanged.

**Tech Stack:** Markdown-only Codex/agent skill files under `E:\ui-skill`.

---

## Files Expected To Change

- Modify: `E:\ui-skill\modes\dynamic-future.md`
- Modify: `E:\ui-skill\modes\simple-designed.md`

## Task 1: Backup Existing Mode Files

- [ ] **Step 1: Create backup**

Run:

```powershell
$ts = Get-Date -Format 'yyyyMMdd-HHmmss'
$backup = "E:\codex_backup\$ts-modes-clarity-pass"
New-Item -ItemType Directory -Path $backup -Force | Out-Null
Copy-Item -LiteralPath 'E:\ui-skill\modes' -Destination (Join-Path $backup 'modes') -Recurse -Force
Write-Output $backup
```

Expected: backup directory path is printed.

## Task 2: Rewrite Mode Files

- [ ] **Step 1: Rewrite all `modes/*.md` files**

Each file must include:

- `## Use When`
- `## Design Intent`
- `## Visual Variables`
- `## Motion Level`
- `## Suitable Tracks`
- `## Not Suitable For`
- `## Required Safeguards`
- `## Do`
- `## Do Not`
- `## Output Notes`

The content must preserve the current two modes:

- Dynamic Future.
- Simple Designed.

## Task 3: Verify Mode Layer

- [ ] **Step 1: Verify required headings**

Run:

```powershell
$required = @('## Use When','## Design Intent','## Visual Variables','## Motion Level','## Suitable Tracks','## Not Suitable For','## Required Safeguards','## Do','## Do Not','## Output Notes')
Get-ChildItem -LiteralPath 'E:\ui-skill\modes' -File | Sort-Object Name | ForEach-Object {
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
Get-ChildItem -LiteralPath 'E:\ui-skill\flows','E:\ui-skill\tracks','E:\ui-skill\rules','E:\ui-skill\output' -File | Select-Object FullName,LastWriteTime
```

Expected: these files are not modified during this pass.

## Self-Review

- Scope: Only `modes/` is edited.
- Requirement coverage: The modes clarity requirement maps to Tasks 2-3.
- Risk: The main risk is turning a mode into a fixed style recipe; preserve the examples-are-not-requirements rule.
