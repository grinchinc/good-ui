# Interaction defaults

Use these as strong defaults, then adapt them to the product and input method.

## Visual ownership

Treat visual customization as a requirement for shipped UI, not a finishing option.

- Style every visible control, field, select, menu, surface, icon, state, and feedback treatment through the project's tokens and visual language.
- Do not leave browser defaults, generated-library demo styling, placeholder appearance, or accidental native chrome in the final interface.
- Reuse accessible behavior from native elements or mature primitives, but own the presentation. Customizing presentation does not mean rebuilding reliable interaction behavior from scratch.
- Inspect the rendered result in context. A class name or theme wrapper is not evidence that the element is actually customized.

## Real icons

- Use an established icon component, inline SVG, local SVG asset, or platform icon system for visual symbols.
- Never substitute Unicode glyphs, emoji, ASCII art, or text characters for icons. This includes check marks, plus signs, close symbols, arrows, hamburger menus, carets, stars, and settings symbols.
- Do not mix arbitrary icon families, weights, fill styles, or stroke conventions. Match icon size, optical weight, and alignment to the component.
- Give icon-only controls an accessible name and a tooltip when the meaning is not immediately obvious. Do not use the icon's source name as visible UI copy.

## Edge clearance

Give every bounded component an explicit internal inset. A component should feel designed from its boundary inward, not like content was dropped into an available box.

- Keep at least 8px between a visible boundary and the nearest content or interactive target in dense UI. Prefer 12px for compact controls, 16px for normal controls, and 24px for spacious surfaces. Keep values on the 4px grid.
- Count the full visual footprint: text, icon box, gap, hit area, focus ring, validation affordance, and any nested surface. Do not inspect only the text baseline.
- Set component padding and gaps at the component level. Do not repair cramped anatomy with arbitrary margins at each usage site.
- For fields and selects, give leading content, label/value text, trailing icons, and the border a balanced inset. Do not let a caret, clear button, or status icon sit visually against the edge.
- If one side is intentionally denser, make it a named variant with a reason. Do not let flex alignment, `width: 100%`, absolute positioning, or an oversized hit area create accidental edge contact.
- Treat a flush treatment as an explicit edge-to-edge variant. Clip, align, and document it intentionally; never arrive there by omission.
- Review screenshots at normal viewing size. If the boundary reads as touching the content even when the measured gap is nonzero, increase the inset or rebalance the component.

Use an edge-clearance pass in the component gallery: inspect all four sides of every bounded primitive and its focus ring, hover layer, and expanded hit area.

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

## Focus hygiene

Prevent accidental focus without hiding legitimate keyboard focus.

- Use `:focus-visible` for the visible focus treatment when the project supports input-modality detection. Keep `:focus:not(:focus-visible)` visually quiet when pointer focus does not need an indicator, while preserving the actual focus target and keyboard behavior.
- Never globally remove outlines without replacing them. Never use `preventDefault` on pointer-down merely to hide a focus ring; it can break focus, dragging, text selection, and assistive technology behavior.
- Do not autofocus by default. Do not focus elements on hover, during passive animation, or simply because a component mounted. Programmatically move focus only when a context change requires it, such as opening a dialog or moving into a newly revealed task.
- Do not add `tabindex` to noninteractive containers to make focus styling easier. Use the correct native element or an accessible primitive.
- When an overlay opens, place focus deliberately; when it closes, return focus to the trigger. When a list, table, or menu mutates, preserve focus or move it to the nearest logical target.
- Keep focus rings visible, intentional, and unclipped. Account for the ring in edge-clearance and overflow decisions.
- Test with pointer, touch, keyboard-only, and screen-reader paths. A focus ring after Tab is correct; an unexplained ring after an ordinary pointer click, hover, mount, or rerender is not.

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
