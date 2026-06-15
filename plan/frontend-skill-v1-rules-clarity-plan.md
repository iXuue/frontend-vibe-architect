# Frontend Skill V1 Rules Clarity Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite priority `rules/` Markdown files so they act as executable decision gates with clear if/then behavior.

**Architecture:** Keep the current layered skill structure. This pass edits only selected files under `rules/`; other layers stay unchanged.

**Tech Stack:** Markdown-only Codex/agent skill files under `E:\ui-skill`.

---

## Files Expected To Change

- Modify: `E:\ui-skill\rules\examples-are-not-requirements.md`
- Modify: `E:\ui-skill\rules\reference-adaptation.md`
- Modify: `E:\ui-skill\rules\verification.md`

## Task 1: Backup Existing Rule Files

- [ ] **Step 1: Create backup**

Run:

```powershell
$ts = Get-Date -Format 'yyyyMMdd-HHmmss'
$backup = "E:\codex_backup\$ts-rules-clarity-pass"
New-Item -ItemType Directory -Path $backup -Force | Out-Null
Copy-Item -LiteralPath 'E:\ui-skill\rules' -Destination (Join-Path $backup 'rules') -Recurse -Force
Write-Output $backup
```

Expected: backup directory path is printed.

## Task 2: Rewrite Priority Rule Files

- [ ] **Step 1: Rewrite selected `rules/*.md` files**

Each edited file must include:

- `## Use When`
- `## Rule`
- `## If`
- `## Then`
- `## Do`
- `## Do Not`
- `## Stop And Ask`
- `## Output Impact`

Content requirements:

- `examples-are-not-requirements.md` must distinguish hard requirements, examples, visual intent, assumptions, and confirmation needs.
- `reference-adaptation.md` must define how to convert references into principles, decision rules, checklists, and verification items without copying.
- `verification.md` must define checks for design-only handoff, implementation-ready handoff, and implemented UI handoff.

## Task 3: Verify Rule Layer

- [ ] **Step 1: Verify required headings**

Run:

```powershell
$required = @('## Use When','## Rule','## If','## Then','## Do','## Do Not','## Stop And Ask','## Output Impact')
$files = @(
  'E:\ui-skill\rules\examples-are-not-requirements.md',
  'E:\ui-skill\rules\reference-adaptation.md',
  'E:\ui-skill\rules\verification.md'
)
$files | ForEach-Object {
  $text = Get-Content -LiteralPath $_ -Raw
  foreach ($h in $required) {
    [PSCustomObject]@{File=(Split-Path $_ -Leaf); Heading=$h; Present=($text -like "*$h*")}
  }
}
```

Expected: every `Present` value is `True`.

- [ ] **Step 2: Verify no out-of-scope files changed by this pass**

Run:

```powershell
Get-ChildItem -LiteralPath 'E:\ui-skill\flows','E:\ui-skill\tracks','E:\ui-skill\modes','E:\ui-skill\output' -File | Select-Object FullName,LastWriteTime
```

Expected: these files are not modified during this pass.

## Self-Review

- Scope: Only selected `rules/` files are edited.
- Requirement coverage: The rules clarity requirement maps to Tasks 2-3.
- Risk: The main risk is making rules too rigid; preserve room for product-specific judgment while keeping clear stop conditions.
