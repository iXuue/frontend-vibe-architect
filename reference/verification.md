# Verification

Before final handoff after implementation, verify:

- Page loads.
- No blank first screen.
- No console errors.
- Main controls respond.
- Text is readable.
- No incoherent overlap.
- No horizontal mobile overflow.
- Motion does not block content.
- Reduced-motion mode is acceptable.
- Dynamic backgrounds do not reduce contrast.
- Performance is acceptable on mobile-sized viewport.

Use `webapp-testing` or the available browser tool for rendered frontend validation.

## Design QA

Check:

- The first viewport reveals the product, offer, tool, or primary workflow.
- The design is not a generic SaaS template.
- Cards are not nested inside cards.
- Glass or blur is used only where it clarifies hierarchy.
- The palette is not a default purple-blue tech gradient unless justified by the product.
- Buttons, inputs, tabs, menus, and controls have clear states.
- Text fits in mobile and desktop viewports.

## Motion QA

Check:

- Reduced-motion users can still understand the UI.
- Motion-heavy effects do not hide core content.
- Scroll effects do not trap or hijack reading.
- Dynamic canvases or backgrounds render nonblank.
- Hover-only affordances have touch or keyboard alternatives where needed.
