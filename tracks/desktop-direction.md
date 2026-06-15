# Track: Desktop Direction

## Use When

Use for desktop software direction, professional tools, creative workspaces, editors, control panels, and document-like applications.

V1 provides design direction unless native desktop implementation details are explicitly in scope.

## Primary Goal

Support focused, high-density, repeated professional work.

The interface should make tools, panels, documents, state, and shortcuts predictable.

## Design Priorities

- Resizable layouts.
- Persistent navigation, menus, or toolbars.
- Keyboard-friendly workflows.
- Higher information density.
- Clear panels, inspectors, and sidebars.
- Multi-window, document, or workspace mental models when relevant.
- Stable state and clear save/export behavior.

## Layout Defaults

- Prefer workspace layouts: toolbar, sidebar, inspector, main canvas, status area.
- Use panes, split views, tabbed documents, and persistent tool regions.
- Keep frequently used tools visible.
- Reserve modal dialogs for focused decisions, not ordinary navigation.
- Let users compare, edit, and switch context efficiently.

## Interaction Defaults

- Support keyboard shortcuts when task repetition implies them.
- Provide right-click/context menus only when they fit the desktop mental model.
- Include drag, resize, selection, undo, redo, save, export, and history concepts when relevant.
- Make selected objects and active panels obvious.
- Preserve state across navigation where appropriate.

## Visual Risk

- Making desktop software look like a landing page.
- Making the interface too sparse for professional work.
- Hiding tools for visual minimalism.
- Ignoring keyboard and precision-pointer workflows.
- Overusing mobile-style bottom navigation or oversized touch controls.

## Do

- Identify the main workspace object: document, canvas, dataset, project, timeline, asset, or system.
- Define persistent tool regions.
- State key shortcuts or repeated actions when relevant.
- Keep density high but organized.
- Clarify native-platform limitations in V1.

## Do Not

- Do not use hero-section thinking inside the working surface.
- Do not hide important tools behind decorative navigation.
- Do not design only for touch unless desktop touch is explicitly required.
- Do not omit save, export, undo, or state behavior when the workflow implies them.
- Do not claim full macOS, Windows, or Linux guideline compliance without review.

## Output Notes

When this track is selected, design options and execution plans must mention:

- Workspace model.
- Persistent regions.
- Main object being edited or managed.
- Keyboard or precision-pointer assumptions.
- State persistence.
- Native-platform boundaries.
