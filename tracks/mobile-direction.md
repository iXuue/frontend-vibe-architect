# Track: Mobile Direction

## Use When

Use for mobile app direction, mobile-first web direction, and mini program direction.

V1 provides design direction only unless the user explicitly requests platform-specific implementation and review.

## Primary Goal

Create a touch-first, short-flow interface direction that respects small screens, attention limits, and platform constraints.

The design should prioritize the user's next action and reduce navigation burden.

## Design Priorities

- Touch-first controls.
- Short, clear flows.
- Safe area awareness.
- Clear primary action.
- Readable typography on small screens.
- Lower animation and rendering budget.
- Fast loading and simple navigation for mini programs.
- Clear empty, loading, error, and permission states.

## Layout Defaults

- Prefer single-column hierarchy.
- Use bottom actions only when they match the platform and task.
- Keep primary content and primary action reachable.
- Avoid dense tables; convert dense data into cards, summaries, lists, or drill-down views.
- Use step flows for complex tasks.
- Keep mini program flows especially short and lightweight.

## Interaction Defaults

- Use tap targets that are large enough for touch.
- Provide immediate feedback for taps, loading, errors, and success.
- Use simple navigation: tabs, stacks, sheets, or short forms.
- Minimize typing where possible.
- Avoid hover-only affordances.

## Visual Risk

- Shrinking a desktop layout into a phone screen.
- Overloading the screen with panels, filters, and dense data.
- Using heavy animation that hurts performance.
- Creating a direction that implies full native guideline compliance without review.
- Ignoring constrained mini program loading and navigation expectations.

## Do

- State whether this is mobile app, mobile web, or mini program direction.
- Keep flows short and task-focused.
- Prioritize touch, readability, and loading behavior.
- Provide lower-motion alternatives.
- Clarify what V1 can and cannot promise.

## Do Not

- Do not claim full native platform compliance without platform-specific review.
- Do not copy desktop navigation patterns directly.
- Do not rely on hover.
- Do not design dense tables as the primary mobile view.
- Do not make visual atmosphere more important than task clarity.

## Output Notes

When this track is selected, design options and execution plans must mention:

- Target mobile surface: app, mobile web, or mini program.
- Primary navigation model.
- Main flow length.
- Touch target and input assumptions.
- Performance and motion limits.
- What remains platform-directional rather than fully specified.
