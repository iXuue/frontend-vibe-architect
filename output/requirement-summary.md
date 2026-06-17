# Output: Requirement Summary

## Use When

Use after `flows/intake.md` and before track, strategy, or mode selection.

The purpose is to separate what the user actually needs from examples, assumptions, taste language, and unresolved decisions.

## Required Shape

```markdown
## Requirement Summary

### 1. Request In One Sentence

- 

### 2. Confirmed Requirements

- Product goal:
- Target users:
- Target platform:
- Required pages or screens:
- Core workflows:
- Hard functional requirements:
- Hard visual requirements:
- Technical constraints:
- Accessibility constraints:
- Acceptance criteria:

### 3. Reference Examples

- User-provided examples:
- What the examples seem to express:
- What must not be copied directly:
- Example status:
  - Hard requirement:
  - Soft reference:
  - Unclear:

### 4. Visual Intent

- Desired feeling:
- Desired complexity level:
- Desired motion level:
- Visual directions to consider:
- Visual directions to avoid:
- User language interpretation:
- Product-fit evidence:
- Strategy-language conflicts:

### 5. Inferred Assumptions

- 

### 6. Open Questions

- Material questions that may change scope, platform, or acceptance criteria:
- Non-blocking questions that can be handled with a stated assumption:

### 7. Potential Conflicts

- Requirement conflicts:
- Example-versus-requirement conflicts:
- Visual-versus-usability conflicts:
- Platform-versus-scope conflicts:

### 8. Routing Readiness

- Ready to choose track:
- Ready to choose strategy:
- Ready to choose visual mode:
- Ready to generate design options:
- Must stop and ask before proceeding:
```

## Do Not Omit

- Do not omit `Reference Examples` when the user used example-based language.
- Do not merge inferred assumptions into confirmed requirements.
- Do not hide conflicts or unresolved scope decisions.
- Do not proceed to design options if a material open question would change platform, required screens, core workflow, or acceptance criteria.
- Do not describe a visual example as a required style unless the user explicitly confirmed it.
- Do not skip product-fit evidence when the user uses subjective design language.
- Do not choose or imply a strategy before the requirement summary has enough product context.
