# Track: Web Product

## Use When

Use for web apps, SaaS tools, dashboards, admin panels, AI tools, creative tools, internal tools, and browser-based workspaces.

Choose this track when the user needs people to complete repeated tasks, manage state, operate data, create content, or use an interactive tool.

## Primary Goal

Help users complete product work efficiently and confidently.

The interface should make navigation, state, controls, and feedback clear before it tries to be visually expressive.

## Design Priorities

- Clear information architecture.
- Stable navigation.
- Repeated-use efficiency.
- Visible system state.
- Empty, loading, error, success, and permission states.
- Dense but readable information hierarchy.
- Keyboard and responsive behavior when relevant.
- Visual identity that supports the workflow without dominating it.

## Layout Defaults

- Prefer app-shell structure: sidebar or top navigation plus main workspace.
- Use persistent toolbars for frequent actions.
- Use panels, tables, lists, inspectors, tabs, and split views when they match the workflow.
- Keep primary actions near the task area.
- Reserve large hero sections for onboarding or empty states, not the main working surface.

## Interaction Defaults

- Provide clear hover, focus, selected, disabled, loading, and error states.
- Support filtering, sorting, search, selection, bulk actions, and undo when the workflow implies them.
- Keep destructive actions confirmable.
- Use progressive disclosure for advanced settings.
- Make repeated actions fast and predictable.

## Visual Risk

- Making the product feel like a marketing page.
- Adding decorative motion that slows repeated work.
- Using low-contrast or overly atmospheric surfaces in dense areas.
- Hiding status, errors, or controls for visual cleanliness.
- Treating an AI tool as only a prompt box without result, history, state, and error design.

## Do

- Identify the primary job the user is trying to complete.
- Design the main working state before decorative sections.
- Include empty, loading, error, and success states when relevant.
- State which controls and components are central to the workflow.
- Keep typography and spacing tight enough for real product use.

## Do Not

- Do not use landing-page composition for operational workflows.
- Do not prioritize cinematic motion over task completion.
- Do not make every workflow a card grid.
- Do not omit state design.
- Do not claim native desktop or mobile behavior unless that platform is explicitly in scope.

## Output Notes

When this track is selected, design options and execution plans must mention:

- Main navigation model.
- Primary workspace structure.
- Core components.
- Key user states.
- Repeated-use efficiency concerns.
- Verification needed for forms, controls, overflow, and responsive behavior.
