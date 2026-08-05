# System and components

Use this reference when defining color, tokens, themes, surfaces, depth, component anatomy, states, or primitive-library use.

## Contents

- [Color](#color)
- [Surfaces and depth](#surfaces-and-depth)
- [Components](#components)

## Color

Use color to support meaning, hierarchy, identity, and state through a systematic and readable model.

- Build a token chain: reference palette values → semantic roles → component usage.
- Keep raw color literals out of components except for isolated artwork or data.
- Define roles such as canvas, surface, elevated surface, text, muted text, border, accent, focus, success, warning, and danger as needed.
- Construct ramps and derived states in OKLCH for more predictable perceptual changes than HSL or RGB.
- Build deliberate lightness progression and reduce chroma near gamut boundaries; do not assume one chroma exists at every hue and lightness.
- Ensure a dependable sRGB result before treating Display P3 as an enhancement. Avoid naive RGB clipping that shifts hue.
- Use APCA as the primary contrast model, with targets appropriate to text size, weight, polarity, and role. Verify every actual foreground/background pair in every theme.
- When explicit WCAG conformance is required, verify it separately rather than treating APCA as the compliance calculation.
- Define explicit foreground or “on-color” tokens for colored surfaces. Do not assume white works on every accent.
- Keep secondary content subordinate without making it faint.

### Solid and alpha colors

- Use solid semantic colors when appearance or contrast must remain exact across backgrounds.
- Use alpha text, icons, and borders as reusable “ink” only across a controlled family of backgrounds. Split dark-on-light and light-on-dark tokens rather than expecting one alpha to cross polarity.
- Use alpha naturally for scrims, overlays, shadows, translucent materials, and state layers over known surfaces.
- Define each reusable alpha token's allowed background range and test the worst composited pair with APCA.
- Increase alpha, split the token, add a controlled backing layer, or use a solid value when any supported background fails.
- Do not place important alpha content directly over uncontrolled images, gradients, or user-selected colors without a contrast-preserving scrim.
- Avoid nested translucency where readability matters. Apply alpha to the color rather than reducing parent opacity when descendants must stay opaque.

### Meaning, themes, and gradients

- Reserve the strongest chroma and contrast for elements that deserve attention.
- Reserve success, warning, and danger colors for their meanings.
- Pair color with text, icon, shape, position, or another durable cue for status and state.
- Derive hover, pressed, selected, and disabled colors from semantic roles and keep adjacent states visibly distinct.
- Treat dark mode as a semantic remapping, not a mechanical inversion. Rebalance lightness, chroma, borders, and elevation.
- Use gradients only when they reinforce the visual direction or meaningful progression.
- Interpolate gradients in OKLab or OKLCH when possible to avoid muddy or unexpectedly dark transitions.
- Shape gradient progression deliberately. Linear stop spacing can concentrate visible change unevenly; use eased stop placement or channel progression when it creates a smoother perceptual result.
- Keep linear gradient progression when uniform change is meaningful, especially in quantitative scales.
- For data visualization, distinguish categories under common color-vision deficiencies and add non-color differentiation when the distinction matters.

Check: Can the palette change while meanings, hierarchy, states, and readability remain intact?

## Surfaces and depth

Use surfaces and depth to clarify spatial and interaction relationships, not to compensate for weak hierarchy.

- Begin with the simplest structure. Content can live directly on the canvas; a card is not the default unit.
- Add a distinct surface only for a meaningful boundary, context, state, interaction region, or layer.
- Use a small elevation system and map each level to a behavior such as base, raised control, sticky region, popover, or modal.
- Prefer the lightest sufficient separation cue: spacing, then fill shift or keyline, then shadow for actual elevation.
- Do not automatically combine contrasting fill, border, radius, and shadow. Make each cue contribute something distinct.
- Keep borders and dividers for structural edges, meaningful adjacency, controls, and data regions.
- Use a crisp 1px hard shadow or inset/outset keyline for a lighter visual edge when appropriate. Unlike a border, it need not affect box geometry.
- Prefer a real border when the edge must participate predictably in sizing or remain available in forced-colors, high-contrast, or print contexts.
- Do not stack a border and hard keyline merely to make an edge stronger.
- Use shadows for overlap or elevation with a coherent light model and restrained spread.
- Keep radii consistent with the shape language and component scale.
- When tightly nested rounded surfaces have visibly related curves, derive the inner radius from the outer radius minus the inset as a starting point. Relax this when layers are separated or intentionally contrast.
- Reduce treatment at inner nesting levels rather than giving each layer equal emphasis.
- Distinguish menus, popovers, and modals from underlying content with suitable elevation and, when needed, a scrim.
- In dark themes, combine controlled surface lightness, borders, and modest shadows rather than exaggerating shadows.
- Use blur and glass only when the background relationship is meaningful and contrast remains reliable.
- Do not make static surfaces look clickable through unnecessary lift or hover styling.

Check: Can every edge, surface change, and elevation level be explained by a real distinction?

## Components

Build consistent, understandable units without unnecessary abstraction or variant complexity.

### Reuse behavior; own the presentation

- Inspect the project's existing components and dependencies before creating a new primitive or adding another library.
- Use native HTML for straightforward behavior, but do not confuse native semantics with mandatory browser-default presentation.
- Avoid conspicuously default browser chrome when it clashes with an otherwise authored interface, especially for selects, date inputs, file inputs, checkboxes, radios, and range controls.
- When native styling is too limited, prefer a mature customizable primitive—such as Base UI, React Aria, Radix, or Ariakit—over rebuilding difficult interaction behavior from generic elements.
- Skin primitives through the project's semantic tokens and component language. Do not copy a library's demo aesthetic or allow several libraries to create competing visual systems.
- Preserve expected keyboard, focus, form, overlay, and touch behavior. A custom-looking control that behaves worse than its native counterpart is unfinished.
- Treat a library's accessibility as a strong foundation, not a guarantee; verify the assembled control in its actual context.
- Do not add a dependency for simple layout, a basic button, or behavior the platform already handles well. Avoid a library whose structure must be heavily fought to produce the intended experience.
- Keep native platform presentation when it provides materially better behavior for the context—commonly some mobile pickers—or when an intentionally utilitarian interface gains little from custom treatment.
- Extend an established primitive before creating a subtly incompatible duplicate.

- Use native semantic elements and established interaction patterns as the foundation.
- Give each component stable anatomy; align and space repeated parts consistently.
- Create reusable components when structure or behavior genuinely repeats. Do not abstract every one-off arrangement.
- Define variants by meaningful role, emphasis, size, or state instead of visual accidents or combinatorial props.
- Name variants semantically, such as primary, danger, compact, or selected, rather than blue or rounded.
- Reference semantic tokens rather than embedding raw color, space, and shadow values.
- Implement only the states relevant to the behavior, including default, hover where hover exists, pressed, focus-visible, disabled, selected, loading, validation, and error.
- Make states perceptible without layout shift. Preserve dimensions when labels change to progress or loading indicators.
- Keep disabled controls recognizable and legible; explain unavailability when the reason matters.
- Match semantics and affordance: buttons perform actions, links navigate, and controls look usable.
- Keep input labels persistent. Use placeholders for examples or hints, not as the only label.
- Place helper text, validation, units, and errors near the field and preserve programmatic relationships.
- Validate whether input is useful for the product, not only whether a parser accepts it. Test whitespace, missing or malformed identifiers, unsupported schemes or formats, boundary lengths, and values that are syntactically valid but operationally meaningless.
- Give icon-only controls familiar symbols, accessible names, and tooltips where helpful. Use text when an icon would remain ambiguous.
- Provide adequate target size and separation without requiring the visible shape to fill the target.
- Support long labels, wrapping, localization, real data, empty values, and narrow containers.
- Avoid making an entire container clickable when it includes nested controls or links.

Check: Does each component stay understandable, consistent, and stable in every context and state?
