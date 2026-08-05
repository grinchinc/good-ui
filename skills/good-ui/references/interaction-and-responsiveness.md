# Interaction and responsiveness

Use this reference when building interaction behavior, motion, responsive adaptation, or accessibility.

## Contents

- [Interaction and motion](#interaction-and-motion)
- [Responsiveness](#responsiveness)
- [Accessibility](#accessibility)

## Interaction and motion

Make interactions predictable, responsive, reversible where possible, and appropriate to the input method.

- Keep primary and commonly used actions visible.
- Reveal repetitive secondary or destructive row actions on hover when permanent display would create noise, but also reveal them on focus or selection and provide a touch path such as an overflow menu.
- Never hide the only route to a core task, required information, or unfamiliar interaction behind hover.
- Reserve space for revealed controls or overlay them intentionally so rows and targets do not shift.
- Give every action immediate and proportional feedback near the affected content.
- Preserve user context: avoid unnecessary navigation, scroll jumps, focus loss, and resets.
- Treat removal, reordering, filtering, and DOM replacement as focus-management events. Preserve focus when the control remains, or move it to the nearest logical target and verify the next keyboard action.
- Prevent duplicate submissions while pending and keep the interface informative rather than inert.
- Use optimistic updates only when success is likely, reversal is easy, and failure can be reconciled clearly.
- Preserve user input on failure, explain the problem usefully, and offer recovery.
- Prefer undo for common reversible actions. Confirm destructive, costly, or difficult-to-reverse actions with non-obvious consequences.
- Define how undo behaves when actions repeat: whether pending operations stack, replace one another, or commit the previous operation. Keep the outcome truthful and understandable.
- Avoid confirmation for low-risk actions merely because it is easy to add.
- Avoid unexpected navigation, autoplay, automatic submission, or changes triggered by hover alone.
- Support mouse, touch, and keyboard; provide alternatives to hover, precision pointing, gestures, and drag-and-drop.
- Manage overlays predictably: place focus appropriately, provide dismissal, return focus to the trigger, and protect unsaved work.
- Announce concise outcomes through a dedicated status region when needed. Do not make a large list, form, or frequently rerendered container live merely because something inside it changes.

### Motion and easing

- Use motion to explain change, preserve spatial relationships, provide feedback, or add intentional delight.
- Prefer interruptible transitions for direct state changes. Reserve keyframes and staged sequences for intentional one-off moments.
- Stagger only infrequent semantic chunks when sequence communicates hierarchy or causality. Do not stagger routine, high-frequency interactions.
- Animate only named properties; never use `transition: all`.
- Pair motion with a static cue such as color, shape, icon, label, or position.
- Choose easing from the action's intent. Direct responses should generally begin promptly and settle smoothly; arrivals, departures, emphasis, and continuous movement may need different curves.
- Avoid linear easing for ordinary interface state changes when it feels mechanical. Keep it for constant-speed movement and progress that should communicate a uniform rate.
- Treat duration and easing as one decision. A curve cannot rescue an overly long transition.
- Keep transitions proportionate to distance and importance. Avoid bounce and elaborate springs unless they support the project's visual language.
- Honor reduced-motion preferences and avoid feedback that shifts layout, obscures the target, or steals focus.

Check: After any action, can the user tell what happened, whether it worked, and what comes next without losing context?

## Responsiveness

Preserve priority, capability, and compositional intent as space and input conditions change.

- Treat responsiveness as adaptation rather than proportional shrinking or indiscriminate stacking.
- Add breakpoints when the composition fails, not merely at familiar device widths.
- Prefer fluid sizes, flexible grids, intrinsic layout, and bounded values over many narrow overrides.
- Preserve core hierarchy and task priority even when navigation, order, grouping, or presentation changes.
- Recompose narrow layouts deliberately rather than turning every multi-column interface into one long undifferentiated column.
- Keep important content and capabilities discoverable on small screens.
- Adapt navigation without changing the underlying information architecture.
- Bound fluid type and spacing so they neither grow indefinitely nor collapse.
- Account for viewport height, safe areas, virtual keyboards, browser chrome, zoom, and dynamic viewport changes.
- Handle tables, timelines, code, and charts with intentional horizontal scrolling, prioritized columns, summaries, or focused detail views rather than generic card conversion.
- Contain necessary horizontal scrolling and signal that more content exists.
- Adapt overlays to context; a desktop dialog may become a sheet or focused full-screen task on narrow screens.
- Provide adequate touch targets while allowing greater pointer density where appropriate.
- Test intermediate widths, not only one phone preset and one wide desktop.
- Stress text zoom, localization, long labels, empty states, and real data.

Check: Does every supported size preserve the same important tasks without feeling like a compromised version of another layout?

## Accessibility

Build accessibility into structure, content, styling, and behavior without allowing compliance theater to dominate every design decision.

- Calibrate rigor to audience, permanence, stakes, and reach.
- Target WCAG 2.2 Level AA and applicable requirements for public, production, essential, or high-stakes products.
- For prototypes, personal tools, ephemeral experiments, and playful toys, prioritize high-impact fundamentals without making exhaustive conformance a prerequisite for exploration.
- Treat accessibility as an important constraint, not the only objective. Preserve deliberate expression while avoiding severe or easily preventable barriers.
- Prefer simple accessible solutions: native elements, clear labels, keyboard operation, visible focus, usable contrast, reduced motion, and sensible structure.
- Use semantic HTML and native controls. Use ARIA to fill real semantic gaps rather than recreating browser behavior.
- Keep document structure, reading order, headings, landmarks, lists, and tables meaningful.
- Make every function keyboard-operable without traps. Keep focus order predictable and manage focus intentionally when context changes.
- Provide a visible focus indicator that remains distinguishable across surfaces and overlays.
- Give every interactive element a concise accessible name that includes its visible label.
- Describe meaningful imagery and hide purely decorative imagery from assistive technology.
- Associate form labels, instructions, helper text, required state, and errors programmatically.
- Announce important dynamic status without moving focus unnecessarily.
- Never communicate information through color, sound, position, shape, or motion alone.
- Support text resizing, zoom, reflow, and adjusted text spacing without clipping or lost controls.
- Provide usable target size, alternatives to complex gestures and dragging, and concurrent input support.
- Respect reduced motion, forced colors, high contrast, and relevant user preferences.
- Avoid flashing, unnecessary autoplay, and inflexible time limits.
- Keep authentication compatible with password managers, paste, autofill, and assistive technology.
- Test with automated checks, keyboard-only use, zoom/reflow, and representative assistive technology when project stakes warrant it. Automated checks alone are insufficient.

Check: Can people perceive, understand, navigate, and operate the complete experience through different senses and input methods?
