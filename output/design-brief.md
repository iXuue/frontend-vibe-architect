# Output: Design Brief

## Use When

Use after the user confirms a design direction, or after the agent makes a low-risk recommendation and explains why user confirmation is not required.

The purpose is to convert a chosen option into a stable design contract that can guide implementation.

## Required Shape

```markdown
## Design Brief

### 1. Chosen Direction

- Direction name:
- Why it was chosen:
- User confirmations:
- Assumptions still in force:

### 2. Product Rationale

- Product goal:
- Primary user need:
- Main workflow supported:
- Success criteria:

### 3. Scope

- Target platform:
- Primary track:
- Secondary track:
- Primary strategy:
- Secondary strategy:
- Product-fit evidence:
- User language interpretation:
- Strategy-language conflicts:
- Included screens or sections:
- Out of scope:
- Non-goals:

### 4. Information Architecture

- Navigation model:
- Screen or section order:
- Primary content hierarchy:
- Repeated content patterns:
- Empty, loading, and error states:

### 5. Component Language

- Core components:
- Control types:
- Card or panel usage:
- Data display patterns:
- Form patterns:
- Icon usage:

### 6. Visual System

- Visual mode:
- Strategy support:
- Color roles:
- Typography roles:
- Spacing rhythm:
- Radius and border rules:
- Shadow, elevation, and material rules:
- Image or media direction:

### 7. Motion And Interaction

- Motion purpose:
- Allowed motion:
- Disallowed motion:
- Micro-interactions:
- Scroll or page transition behavior:
- Reduced-motion fallback:

### 8. Responsive And Platform Behavior

- Desktop behavior:
- Tablet behavior:
- Mobile behavior:
- Minimum layout constraints:
- Touch or pointer considerations:

### 9. Accessibility And Usability

- Readability requirements:
- Contrast considerations:
- Keyboard or focus expectations:
- Motion sensitivity:
- Error prevention:

### 10. Risks And Checks

- Design risks:
- Implementation risks:
- Verification required:
- Items not yet verified:
```

## Do Not Omit

- Do not omit user confirmations for broad or visually ambiguous work.
- Do not omit assumptions and non-goals.
- Do not include visual choices that cannot be traced to the requirement, selected option, or user confirmation.
- Do not claim platform-native compliance unless specifically verified.
- Do not describe motion only as decoration; connect it to feedback, orientation, hierarchy, or product feeling.
- Do not omit the confirmed strategy and how user design language was interpreted.
- Do not let user design language override the selected strategy without an explicit user confirmation.
