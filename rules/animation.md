# Rule: Animation

Use GSAP skills for implementation guidance:

- `gsap-core`: basic tweens and simple UI motion.
- `gsap-timeline`: sequenced entrances and transitions.
- `gsap-scrolltrigger`: scroll storytelling and scroll-linked animation.
- `gsap-plugins`: Flip, Draggable, SplitText, ScrambleText, MorphSVG, MotionPath.
- `gsap-utils`: mapping input values to animation values.
- `gsap-react`: React-safe animation lifecycle.
- `gsap-performance`: performance constraints.
- `gsap-frameworks`: Vue, Svelte, and other framework adaptation.

Motion rules:

- Prefer transform and opacity.
- Avoid animating layout properties unless necessary.
- Do not hide core content until animation fires.
- Use reduced-motion fallback.
- Use mobile fallback for heavy blur, particles, pinning, and scroll-linked effects.
- Motion must communicate hierarchy, state, causality, data, or spatial continuity.
