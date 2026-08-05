# Component system

Create a small, coherent system whenever the task introduces a new product surface or substantially revises an existing one.

## Establish the foundation

- Inspect and extend existing tokens before creating new ones.
- Define semantic roles for spacing, control sizes, typography, color, focus, surfaces, borders, elevation, radii, and motion.
- Keep raw values inside the token layer or isolated artwork, not scattered through components.
- Choose variants by role, emphasis, size, density, or state. Avoid APIs that encode visual accidents or every possible prop combination.
- Prefer semantic HTML and mature primitives for difficult behavior. Do not rebuild complex menus, dialogs, comboboxes, or focus management from generic elements when a reliable primitive already exists.

## Build real components

For each reusable interactive component, define:

1. Stable anatomy and semantic markup.
2. Visual sizes and spacing from the shared scale.
3. An adequate hit area that does not damage neighboring interactions.
4. Relevant default, hover, focus-visible, pressed, selected, disabled, loading, validation, and error states.
5. Long-label, empty, overflow, narrow-width, and localization behavior where relevant.
6. Keyboard, touch, focus recovery, and reduced-motion behavior.

Use real product content and actual component imports. Do not create a separate “designer version” that drifts from production behavior.

## Create the review surface

For substantial UI work, create a dev-only component review surface using the project's existing route, Storybook, or component tooling. Add new tooling only when the project will benefit from it.

Show the actual components in isolation with:

- Foundation tokens and spacing examples.
- Primitive and composed component variants.
- Relevant control sizes and densities.
- Hover, focus-visible, pressed, selected, disabled, loading, validation, and error states.
- Long labels, empty values, realistic content, and narrow containers.
- Light/dark themes or other supported modes.
- Keyboard and overlay behavior that can be exercised directly.

Make the surface useful to a designer: it should expose the decisions and let them compare real states, not merely document component names.

## Add a dev overlay only when useful

When asked to create dev controls, place them in the actual product surface and wire them to real state, real data, and production components. Keep them temporary and clearly separate from user-facing UI.

- Gate the overlay behind a development environment, feature flag, route, or explicit keyboard toggle.
- Keep controls keyboard-accessible and avoid covering the surface being evaluated.
- Use it to test density, motion, content, theme, component variants, and layout decisions in context.
- Do not let overlay state alter persisted user data or production defaults.
- Remove it or leave it behind a deliberate development-only gate before delivery.
