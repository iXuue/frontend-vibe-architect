# Motion Language

## Use When

Use when the user asks for dynamic, alive, smooth, interactive, immersive, playful, cinematic, scroll-driven, or animated interface behavior.

## What User Might Say

- Make it dynamic.
- It should feel alive.
- Add smooth interactions.
- I want it cinematic.
- Make it immersive.
- It should not feel static.

## What It May Mean

- Clear feedback on hover, press, focus, selection, loading, or completion.
- Subtle transitions between states.
- Motion that guides attention.
- Scroll or page transitions for narrative surfaces.
- Data updates that feel understandable.
- A more expressive product personality.

## What It Does Not Necessarily Mean

- Heavy animation.
- Constant movement.
- GSAP by default.
- Scroll hijacking.
- Particle backgrounds.
- Cinematic transitions on every interaction.
- Motion that blocks task completion.

## Clarifying Questions

- Should motion improve usability, brand feeling, or both?
- Which moments should move?
- Is the product used repeatedly for focused work?
- Are reduced-motion users or low-performance devices important?

## Design Variables To Adjust

- Motion purpose.
- Trigger type.
- Duration.
- Easing.
- Stagger.
- Transition scope.
- Idle movement.
- Reduced-motion fallback.
- Performance budget.

## Suitable Tracks

- `tracks/landing-brand.md` for scroll storytelling and memorable first impression.
- `tracks/web-product.md` for feedback and state transitions.
- `tracks/mobile-direction.md` for tactile transitions and completion feedback.
- `tracks/data-visualization.md` for data changes, not decorative motion.
- `tracks/desktop-direction.md` for precise, restrained interaction feedback.

## Suitable Modes

- `modes/dynamic-future.md` when motion is central to feeling or orientation.
- `modes/simple-designed.md` when motion should stay subtle and functional.

## Risks

- Motion competing with content.
- Motion reducing scan speed.
- Poor performance.
- Accessibility problems for motion-sensitive users.
- Using animation to hide weak layout.

## Output Guidance

- State the purpose of motion before naming effects.
- Separate allowed and disallowed motion.
- Include reduced-motion fallback.
- If implementation is requested, route through `rules/animation.md`.
