# Flow: Choose Track

## Purpose

Choose the product or platform path that should guide design decisions.

## When To Read

Read after `flows/intake.md` and before generating design options.

## Inputs

- Requirement summary.
- Target platform.
- Product goal.
- Required pages or screens.
- Core workflows.
- User session type: short visit, repeated work, monitoring, creation, transaction, presentation.

## Do

Choose one primary track and optional secondary track:

- `tracks/web-product.md`: web apps, SaaS tools, dashboards, admin panels, AI tools, creative tools.
- `tracks/landing-brand.md`: websites, landing pages, launch pages, brand surfaces.
- `tracks/mobile-direction.md`: mobile app and mini program direction.
- `tracks/desktop-direction.md`: desktop software direction.
- `tracks/data-visualization.md`: data dashboards, monitoring, large-screen displays.

Decide by answering:

- Is the surface brand-led, product-led, or hybrid?
- Is the main job browsing, creating, monitoring, operating, buying, learning, or presenting?
- Is the session short or repeated?
- Does the platform need touch, keyboard, dense tables, or large-screen viewing?
- Would heavy motion help understanding or distract from work?

State the chosen track before generating design options.

## Do Not

- Do not default every request to a landing page.
- Do not treat a dashboard, admin panel, or tool as a marketing surface.
- Do not promise full native mobile, mini program, or desktop compliance in V1.
- Do not choose a track only because of visual style.

## Output

Produce:

- Primary track.
- Optional secondary track.
- Reason for choosing the track.
- Track-specific risks.
- Track files that must be read next.

## Stop And Ask

Stop and ask when:

- Platform is ambiguous and would change the structure.
- The request mixes multiple products or surfaces that need separate tracks.
- The user expects implementation in a platform outside V1's design-direction boundary.
