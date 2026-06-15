# Rule: Verification

## Use When

Use before final handoff for:

- Design-only responses.
- Design option responses.
- Implementation-ready frontend execution plans.
- Implemented frontend UI.

## Rule

Every handoff must match the stage of work.

Do not claim implementation quality, browser behavior, responsiveness, accessibility, or motion safety unless it has been checked or explicitly listed as unverified.

## If

If the work is design-only, verify the design logic.

If the work is implementation-ready, verify that the steps are specific enough to execute.

If the UI has been implemented, verify the rendered result with available browser or testing tools.

If verification cannot be run, state what was not verified.

## Then

Apply the right gate:

### Design Logic Gate

- Requirement summary exists.
- Track is stated.
- Mode is stated.
- Examples are separated from hard requirements.
- Design options explain fit and risk.
- Broad or ambiguous work asks for user direction.

### Execution Readiness Gate

- Page or screen structure exists.
- Component breakdown exists.
- Visual token guidance exists.
- Motion and interaction rules exist.
- Responsive behavior rules exist.
- Implementation order exists.
- Verification steps exist.

### Rendered UI Gate

- Page loads.
- No blank first screen.
- No console errors.
- Main controls respond.
- Text is readable.
- No incoherent overlap.
- No horizontal mobile overflow.
- Motion does not block content.
- Reduced-motion behavior is acceptable.
- Dynamic backgrounds do not reduce contrast.
- Performance is acceptable on a mobile-sized viewport.

## Do

- Use `webapp-testing` or the available browser tool for rendered frontend validation when implementation exists.
- Check text overflow and layout overlap on both desktop and mobile when possible.
- Check reduced-motion behavior for motion-heavy directions.
- Check that first viewport reveals the product, offer, tool, or primary workflow.
- Check that buttons, inputs, tabs, menus, and controls have clear states.
- State residual risk when verification is incomplete.

## Do Not

- Do not say "verified" when only the plan was inspected.
- Do not ignore accessibility, contrast, reduced motion, or mobile overflow.
- Do not treat a beautiful screenshot as sufficient if controls, states, and errors were not checked.
- Do not omit verification steps from implementation-ready output.
- Do not hide known gaps or unverified assumptions.

## Stop And Ask

Stop and ask the user when:

- Verification requires running a local app but no run command or target is known.
- The implementation target is outside the confirmed scope.
- A visual direction requires assets, platform behavior, or dependencies that are not approved.
- A failed verification would require changing requirements or design direction.

## Output Impact

Final responses must distinguish:

- Verified.
- Not verified.
- Not applicable.
- Remaining risks.

Implementation-ready plans must include verification steps even before implementation begins.
