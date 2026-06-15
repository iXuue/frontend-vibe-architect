# Frontend Skill V1 Router Table Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite `SKILL.md` into a compact pseudo-code router that tells the agent which flow, track, mode, rule, and output files to read.

**Architecture:** Keep the current layered skill structure. This pass edits only `SKILL.md`; all sublayer files stay unchanged.

**Tech Stack:** Markdown-only Codex/agent skill file under `E:\ui-skill`.

---

## Files Expected To Change

- Modify: `E:\ui-skill\SKILL.md`

## Task 1: Backup Existing Entry File

- [ ] **Step 1: Create backup**

Run:

```powershell
$ts = Get-Date -Format 'yyyyMMdd-HHmmss'
$backup = "E:\codex_backup\$ts-skill-router-table-pass"
New-Item -ItemType Directory -Path $backup -Force | Out-Null
Copy-Item -LiteralPath 'E:\ui-skill\SKILL.md' -Destination (Join-Path $backup 'SKILL.md') -Force
Write-Output $backup
```

Expected: backup directory path is printed.

## Task 2: Rewrite `SKILL.md`

- [ ] **Step 1: Replace entry content with pseudo-code router**

`SKILL.md` must include:

- Frontmatter.
- Purpose.
- Required workflow.
- Routing table.
- Stop conditions.
- Hard rules.

Routing table must include:

- Intake routing.
- Track routing.
- Mode routing.
- Rule routing.
- Output routing.

## Task 3: Verify Router

- [ ] **Step 1: Verify required sections**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\SKILL.md' -Pattern 'Required Workflow|Routing Table|Track Routing|Mode Routing|Rule Routing|Output Routing|Stop Conditions|Hard Rules'
```

Expected: matching lines for every section.

- [ ] **Step 2: Verify all layer references**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\SKILL.md' -Pattern 'flows/intake.md|tracks/web-product.md|tracks/landing-brand.md|tracks/mobile-direction.md|tracks/desktop-direction.md|tracks/data-visualization.md|modes/dynamic-future.md|modes/simple-designed.md|rules/examples-are-not-requirements.md|rules/reference-adaptation.md|rules/animation.md|rules/verification.md|rules/requirement-change-control.md|output/requirement-summary.md|output/design-options.md|output/design-brief.md|output/frontend-execution-plan.md'
```

Expected: matching lines for all referenced layer files.

- [ ] **Step 3: Verify no out-of-scope files changed by this pass**

Run:

```powershell
Get-ChildItem -LiteralPath 'E:\ui-skill\flows','E:\ui-skill\tracks','E:\ui-skill\modes','E:\ui-skill\rules','E:\ui-skill\output' -File | Select-Object FullName,LastWriteTime
```

Expected: these files are not modified during this pass.

## Self-Review

- Scope: Only `SKILL.md` is edited.
- Requirement coverage: The router table requirement maps to Tasks 2-3.
- Risk: The router must stay compact; detailed design rules remain in sublayer files.
