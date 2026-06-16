# Material Language

## Use When

Use when the user describes texture, depth, surface, glass, softness, sharpness, tactile quality, transparency, shadow, glow, or visual weight.

## What User Might Say

- It should have texture.
- Make it feel light and transparent.
- I want a glassy feeling.
- Give it depth.
- Make it soft and refined.
- It should feel solid and stable.

## What It May Mean

- Adjust surface hierarchy.
- Use borders, shadows, opacity, blur, or layering to show depth.
- Make primary controls feel tactile.
- Separate background, container, and content layers.
- Give the product a clearer visual material system.

## What It Does Not Necessarily Mean

- Glassmorphism everywhere.
- Blur on all panels.
- Dark background.
- Glow effects.
- Heavy shadows.
- Low contrast.
- Decorative material that weakens readability.

## Clarifying Questions

- Should material help hierarchy or mainly create atmosphere?
- Which areas need depth: navigation, cards, modals, controls, or background?
- Is readability more important than surface effect?
- Should the interface feel light, solid, soft, sharp, tactile, or neutral?

## Design Variables To Adjust

- Background layer.
- Surface opacity.
- Border contrast.
- Shadow strength.
- Blur amount.
- Highlight and reflection.
- Radius.
- Elevation.
- Content contrast.

## Suitable Tracks

- `tracks/landing-brand.md` for expressive atmosphere.
- `tracks/web-product.md` for surface hierarchy and state clarity.
- `tracks/mobile-direction.md` for tactile surfaces.
- `tracks/desktop-direction.md` for stable panes and tool surfaces.
- `tracks/data-visualization.md` only when material does not reduce chart readability.

## Suitable Modes

- `modes/dynamic-future.md` when material supports atmosphere or spatial feeling.
- `modes/simple-designed.md` when material should be restrained and readable.

## Risks

- Low contrast from transparency or blur.
- One-note visual styling.
- Too many layered cards.
- Material effects that ignore product purpose.
- Performance cost from excessive blur.

## Output Guidance

- Describe material as a hierarchy system, not a decoration.
- State where material effects are allowed.
- State where plain surfaces are required for readability.
- Connect material choices to product context.
