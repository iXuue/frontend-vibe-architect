# Output: Frontend Execution Plan

## Use When

Use after a design brief exists and the user wants implementation-ready frontend design steps.

The purpose is to turn the design brief into a practical build sequence that an agent or developer can follow without inventing new visual direction mid-build.

## Required Shape

```markdown
## Frontend Execution Plan

### 1. Build Target

- Target platform:
- Framework or stack, if known:
- Existing files or app areas:
- New files or app areas:
- Assets required:
- External dependencies:

### 2. Page Or Screen Structure

- Screen or page list:
- Section order:
- Navigation structure:
- Primary user path:
- Secondary paths:
- Empty, loading, error, and success states:

### 3. Component Breakdown

- Layout components:
- Navigation components:
- Content components:
- Input or control components:
- Feedback components:
- Data display components:
- Reusable primitives:

### 4. Visual Token Guidance

- Color roles:
- Typography scale:
- Spacing scale:
- Radius:
- Borders:
- Shadow, elevation, and material:
- Iconography:
- Image and media treatment:

### 5. Motion And Interaction Rules

- Motion library, if needed:
- Entrance or page transitions:
- Hover, press, focus, and selected states:
- Scroll behavior:
- Data or state change animation:
- Timing and easing guidance:
- Reduced-motion fallback:

### 6. Responsive Behavior Rules

- Desktop:
- Tablet:
- Mobile:
- Minimum width behavior:
- Content overflow rules:
- Touch target rules:

### 7. Implementation Order

1. Establish layout shell and routing or screen structure.
2. Build static content hierarchy without final motion.
3. Add reusable components and state variants.
4. Apply visual tokens and responsive constraints.
5. Add motion and interaction details.
6. Add empty, loading, error, and success states.
7. Run visual and functional verification.

### 8. Verification Steps

- Requirement trace:
- Desktop viewport check:
- Mobile viewport check:
- Text overflow check:
- Interaction state check:
- Reduced-motion check:
- Accessibility smoke check:
- Screenshot or rendered UI evidence:
- Unverified items:
```

## Do Not Omit

- Do not omit component breakdown.
- Do not omit responsive behavior.
- Do not omit empty, loading, error, and success states when the interface is interactive.
- Do not omit verification steps.
- Do not add implementation tasks that are not traceable to the requirement, selected direction, or design brief.
- Do not treat visual polish as complete until readability, layout stability, interaction states, and reduced-motion behavior are considered.
