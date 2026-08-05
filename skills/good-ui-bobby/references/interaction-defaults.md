# Interaction defaults

Use these as strong defaults, then adapt them to the product and input method.

## Grid and control scale

- Use 4px as the atomic spacing unit and 8px as the preferred macro rhythm.
- Prefer spacing, insets, radii, line heights, and offsets that land on the grid. Treat one-off values as a signal to inspect the structure.
- Prefer visual control sizes of 24px, 32px, 40px, 48px, and 56px. Use larger sizes when the context needs them; use smaller sizes only for a compelling, product-specific reason.
- Separate the visible control box from the effective interaction target. A 24px icon button may have a larger hit area and still remain visually compact.
- Preserve stable dimensions when labels change, controls enter loading state, or secondary actions are revealed.

## Hit areas

When the project uses Tailwind or shadcn/ui, prefer the `hit-area` utilities from the [hit-area registry](https://bazza.dev/craft/2026/hit-area):

```sh
npx shadcn@latest add https://bazza.dev/r/hit-area
```

Use `hit-area-*`, side-specific utilities, or axis utilities to:

- Enlarge small icon buttons, checkboxes, and compact controls without changing layout.
- Bridge intentional gaps between tabs, sidebar rows, or adjacent controls that should feel continuous.
- Make a whole cell or row a comfortable target when the semantic control remains the actual interactive element.

Check that expanded areas do not overlap an unrelated interactive element, steal pointer events, or make a neighboring control difficult to reach. Use `hit-area-debug` while tuning and remove it before delivery. Verify pointer, touch, keyboard focus, and screen-reader semantics separately; a larger pointer target does not replace an accessible name or visible focus indicator.

## State model

Treat hover and pressed feedback as required for interactive elements unless the input method or product context makes a state genuinely meaningless. Add focus-visible independently of hover. Add selected, disabled, loading, validation, and error states when the component can enter them.

- Make state changes perceptible through a considered combination of color, surface, border, icon, label, position, or motion.
- Keep states project-appropriate. Do not apply a universal color or scale treatment across unrelated products.
- Keep hover feedback pointer-specific; never make hover the only route to an action or piece of information.
- Make pressed feedback immediate and restrained. A small transform, surface shift, shadow change, or color change is enough when it suits the component.
- Keep disabled controls legible and non-interactive. Preserve layout and explain unavailability when the reason matters.

## Motion and continuity

Show the transition between meaningful states rather than snapping between unrelated screenshots of the same object.

- Preserve element identity when a control grows, moves, expands, collapses, filters, or changes emphasis.
- Prefer interruptible transitions for interactive state changes. Animate named properties such as `transform`, `opacity`, `color`, `background-color`, `border-color`, `box-shadow`, or `clip-path`; never use `transition: all`.
- Let small things get bigger, left things move right, and overlays originate from their trigger when that explains the relationship.
- Use the project's existing motion primitive when one exists. Otherwise use CSS transitions, the View Transition API, or a suitable layout/motion utility according to the stack.
- Keep routine feedback short and responsive. Reserve elaborate sequences and bounce for a deliberate product language.
- Honor `prefers-reduced-motion` by removing or minimizing nonessential movement while preserving the state change and feedback.
- Do not animate when movement would obscure a critical update, create disorientation, cause layout instability, or waste time during high-frequency updates.

## shadcn/ui

Use [shadcn/ui](https://ui.shadcn.com/docs/installation) as a starting point when the project supports it:

- Inspect `components.json`, the package manager, Tailwind setup, existing primitives, and framework before installing anything.
- Prefer the project's existing primitives and add only what the task needs.
- Restyle generated components through the project's tokens, density, shape, typography, and motion language.
- Do not copy shadcn's demo composition or treat its default aesthetic as a requirement.
- Preserve the primitive's keyboard, focus, form, overlay, and touch behavior. Verify the assembled control in its actual context.
