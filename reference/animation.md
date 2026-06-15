# Animation

Use GSAP skills for implementation guidance:

- `gsap-core`: basic tweens and simple UI motion.
- `gsap-timeline`: sequenced entrances and transitions.
- `gsap-scrolltrigger`: scroll storytelling and scroll-linked animation.
- `gsap-plugins`: Flip, Draggable, SplitText, ScrambleText, MorphSVG, MotionPath.
- `gsap-utils`: mapping input values to animation values.
- `gsap-react`: React-safe animation lifecycle.
- `gsap-performance`: performance constraints.
- `gsap-frameworks`: Vue, Svelte, and other framework adaptation.

## Motion Rules

- Prefer transform and opacity.
- Avoid animating layout properties unless necessary.
- Do not hide core content until animation fires.
- Use reduced-motion fallback.
- Use mobile fallback for heavy blur, particles, pinning, and scroll-linked effects.
- Motion must communicate hierarchy, state, causality, data, or spatial continuity.

## When To Use Motion

Use motion for:

- Revealing hierarchy.
- Connecting a user action to a result.
- Showing state changes.
- Guiding attention.
- Explaining data flow.
- Creating brand atmosphere when the product surface can support it.

Avoid motion when:

- The user is doing repetitive operational work.
- The animation delays task completion.
- The content becomes harder to read.
- The mobile fallback would remove the main experience.
- The effect exists only because it looks futuristic.
