# Frontend Skill V1 Flows And Output Clarity Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite `flows/` and `output/` Markdown files so they behave like executable agent instructions with clear inputs, actions, outputs, and stop conditions.

**Architecture:** Keep the current layered folder structure. This pass only edits `flows/*.md` and `output/*.md`; it does not change `SKILL.md`, `tracks/`, `modes/`, or `rules/`.

**Tech Stack:** Markdown-only Codex/agent skill files under `E:\ui-skill`.

---

## Files Expected To Change

- Modify: `E:\ui-skill\flows\intake.md`
- Modify: `E:\ui-skill\flows\choose-track.md`
- Modify: `E:\ui-skill\flows\design-options.md`
- Modify: `E:\ui-skill\flows\execution-steps.md`
- Modify: `E:\ui-skill\flows\handoff.md`
- Modify: `E:\ui-skill\output\requirement-summary.md`
- Modify: `E:\ui-skill\output\design-options.md`
- Modify: `E:\ui-skill\output\design-brief.md`
- Modify: `E:\ui-skill\output\frontend-execution-plan.md`

## Task 1: Backup Existing Files

- [ ] **Step 1: Create backup**

Run:

```powershell
$ts = Get-Date -Format 'yyyyMMdd-HHmmss'
$backup = "E:\codex_backup\$ts-flows-output-clarity-pass"
New-Item -ItemType Directory -Path $backup -Force | Out-Null
Copy-Item -LiteralPath 'E:\ui-skill\flows' -Destination (Join-Path $backup 'flows') -Recurse -Force
Copy-Item -LiteralPath 'E:\ui-skill\output' -Destination (Join-Path $backup 'output') -Recurse -Force
Write-Output $backup
```

Expected: backup directory path is printed.

## Task 2: Rewrite Flow Files

- [ ] **Step 1: Rewrite all `flows/*.md` files**

Each file must include:

- `## Purpose`
- `## When To Read`
- `## Inputs`
- `## Do`
- `## Do Not`
- `## Output`
- `## Stop And Ask`

The content must preserve current behavior:

- Requirement intake separates hard requirements, examples, visual intent, forbidden directions, assumptions, and questions.
- Track choice selects one primary track and optional secondary track.
- Design options produce 2-4 options when direction is not precise.
- Execution steps require page structure, component breakdown, tokens, motion, responsive behavior, implementation order, and verification.
- Handoff distinguishes design-only and implementation-ready outputs.

## Task 3: Rewrite Output Templates

- [ ] **Step 1: Rewrite all `output/*.md` files**

Each output template must include:

- `## Use When`
- `## Required Shape`
- `## Do Not Omit`

Templates must be strict enough that another agent can follow them without guessing.

## Task 4: Verify Clarity Pass

- [ ] **Step 1: Verify flow headings**

Run:

```powershell
Select-String -Path 'E:\ui-skill\flows\*.md' -Pattern '## Purpose|## When To Read|## Inputs|## Do|## Do Not|## Output|## Stop And Ask'
```

Expected: each flow file contains all seven headings.

- [ ] **Step 2: Verify output headings**

Run:

```powershell
Select-String -Path 'E:\ui-skill\output\*.md' -Pattern '## Use When|## Required Shape|## Do Not Omit'
```

Expected: each output file contains all three headings.

- [ ] **Step 3: Verify no out-of-scope files changed by this pass**

Run:

```powershell
Get-ChildItem -LiteralPath 'E:\ui-skill\tracks','E:\ui-skill\modes','E:\ui-skill\rules' -File | Select-Object FullName,LastWriteTime
```

Expected: these files are not modified during this pass.

## Self-Review

- Scope: Only `flows/` and `output/` are edited.
- Requirement coverage: The clarity-pass requirement maps to Tasks 2-4.
- Risk: The main risk is over-formatting templates so much that they become hard to use; keep fields strict but concise.
