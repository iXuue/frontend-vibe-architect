# Frontend Skill V1 Reference Deprecation Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Mark the old `reference/` folder as deprecated without deleting it.

**Architecture:** Documentation-only pass. Add `reference/README.md`; do not modify or delete existing reference files.

**Tech Stack:** Markdown documentation under `E:\ui-skill`.

---

## Files Expected To Change

- Create: `E:\ui-skill\reference\README.md`

## Task 1: Create Deprecation Notice

- [ ] **Step 1: Add `reference/README.md`**

Write a short deprecation notice explaining that the active skill structure is now:

- `flows/`
- `tracks/`
- `modes/`
- `rules/`
- `output/`
- `examples/`

The notice must also state that deletion requires separate explicit user confirmation.

## Task 2: Verify Notice

- [ ] **Step 1: Verify file exists and contains required terms**

Run:

```powershell
Select-String -LiteralPath 'E:\ui-skill\reference\README.md' -Pattern 'Deprecated|flows/|tracks/|modes/|rules/|output/|examples/|explicit user confirmation'
```

Expected: matching lines for the deprecation notice and active folders.

- [ ] **Step 2: Verify no files were deleted**

Run:

```powershell
Get-ChildItem -LiteralPath 'E:\ui-skill\reference' -File | Select-Object Name,Length
```

Expected: existing reference files are still present.

## Self-Review

- Scope: Adds one README file only.
- Deletion safety: No files are deleted.
- Requirement coverage: Deprecation notice maps to Task 1 and verification maps to Task 2.
