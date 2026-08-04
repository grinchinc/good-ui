# UI Fundamentals Reference

Use these principles to create or revise interfaces without imposing a house style. Preserve intentional project character; correct accidental inconsistency and weak execution.

## Contents

1. [Intentionality](#1-intentionality)
2. [Hierarchy](#2-hierarchy)
3. [Layout](#3-layout)
4. [Spacing](#4-spacing)
5. [Typography](#5-typography)
6. [Color](#6-color)
7. [Surfaces and depth](#7-surfaces-and-depth)
8. [Components](#8-components)
9. [Interaction and motion](#9-interaction-and-motion)
10. [Responsiveness](#10-responsiveness)
11. [Accessibility](#11-accessibility)
12. [Polish](#12-polish)
13. [Restraint](#13-restraint)
14. [Slop prevention](#14-slop-prevention)

## 1. Intentionality

Make the UI feel guided by a coherent point of view rather than assembled from individually reasonable defaults.

- Establish a simple visual thesis from the product's purpose, audience, content, and desired tone.
- Let the thesis inform typography, color, density, shape, imagery, and motion.
- Respect existing brand and project conventions. Extend them rather than casually replacing them.
- Avoid unconscious defaults and fashionable clichés, especially interchangeable SaaS layouts.
- Do not equate good design with minimal, neutral, spacious, or corporate. Expressive, dense, playful, and unconventional interfaces can be highly competent.
- Repeat a small number of visual ideas so the experience feels authored and cohesive.
- Make decorative choices reinforce identity, hierarchy, meaning, or delight.
- Correct accidental inconsistency without sanding away deliberate character.
- Prefer a clear direction over a timid mixture of visual styles.

Check: Can someone explain why this interface looks this way beyond “it looks modern”?

## 2. Hierarchy

Make importance, relationships, and the intended path apparent before the user reads every word.

- Give each screen or region one clear focal point and primary purpose.
- Make the most important information and action visually dominant; do not let several elements compete for first attention.
- Reflect actual user priorities rather than internal organizational structure.
- Combine size, weight, contrast, position, spacing, and color. Do not rely on font size or color alone.
- Use a restrained number of hierarchy levels with perceptible differences.
- Keep supporting content subordinate without making it faint or difficult to read.
- Use proximity and shared alignment to communicate relationships.
- Distinguish primary, secondary, and tertiary actions consistently.
- Reveal advanced or infrequent options progressively when showing everything weakens the main path.
- Preserve hierarchy during responsive reflow instead of creating an undifferentiated vertical stack.
- Use accent color selectively so it retains attention-directing power.

### Prefer structure over enclosure

- Use spacing, alignment, typography, contrast, and proximity as the first tools for structure.
- Add borders, dividers, fills, and containing shapes only for meaningful boundaries, groups, interactions, or context changes.
- Fix the underlying layout before adding a card or separator to rescue weak hierarchy.
- Avoid containers nested inside containers. When nesting is necessary, reduce the treatment of inner levels.
- Do not give every nested layer its own fill, border, radius, and shadow.
- Let content sit directly on the canvas when no enclosure is needed.

Check: Does a glance reveal what matters, what belongs together, and what to do next?

## 3. Layout

Give content a clear spatial logic that feels stable, connected, and easy to scan.

- Establish an underlying grid or small set of alignment lines. Avoid independently positioned elements.
- Use as few alignment axes as the composition reasonably permits.
- Align related elements precisely; use asymmetry deliberately rather than accidentally.
- Choose widths for the material. Prose, forms, data tables, and immersive media do not need the same container.
- Constrain long-form text to a comfortable reading measure.
- Do not make every section full-width because the viewport allows it.
- Treat whitespace as composition, but match density to the task; more space is not automatically better.
- Prefer natural flow and flexible constraints over brittle fixed positioning.
- Use centered composition for short, focused material. Prefer left alignment for scanning and complex information.
- Give prominent elements enough surrounding space to carry their visual weight.
- Balance the whole screen, not only each component in isolation.
- Test with real content lengths rather than placeholder-perfect copy.

Check: Does every element have a clear spatial relationship to the elements around it?

## 4. Spacing

Use space to create rhythm, communicate relationships, and establish an appropriate density.

- Use a deliberate scale or small family of recurring values instead of arbitrary gaps.
- Keep space within a group smaller than space between groups, and group spacing smaller than major section spacing.
- Keep repeated components and repeated relationships spatially consistent.
- Choose component padding from its content and intended density rather than applying one universal value.
- Make horizontal and vertical padding feel balanced without requiring numeric equality.
- Avoid blanket uniformity where every gap is identical and uncontrolled variety where every gap is unique.
- Match density to context. Productivity interfaces may need compact efficiency; focused or expressive experiences may need more breathing room.
- Preserve adequate target size and readability even in compact layouts.
- Treat unexpected one-off spacing values as a signal to inspect the underlying structure.
- Prefer shared spacing tokens once a recurring relationship is established.

Check: Can the spacing alone reveal which things belong together and which begin a new idea?

## 5. Typography

Make content readable, hierarchy unmistakable, and project character coherent.

- Choose typefaces for content, audience, and tone; prioritize readability for interface and body text.
- Use a restrained type system. One family with a useful weight range may be enough; add another only for a clear role.
- Define semantic text styles instead of styling headings and labels ad hoc.
- Create hierarchy with meaningful differences in size, weight, line height, and spacing.
- Keep body and interface text comfortably readable. Reserve very small text for genuinely secondary information.
- Set line height relative to size and measure: prose generally needs more leading; large headings can be tighter.
- Constrain prose line length and avoid both sprawling and excessively narrow columns.
- Use weight deliberately. Do not make every label bold or depend on very light weights for hierarchy.
- Keep uppercase text short. Tracked uppercase can suit navigation, metadata, and concise labels when the visual language calls for it.
- Do not invent eyebrow or kicker labels merely to decorate headings. Use them only for real category, sequence, or context.
- Keep body tracking near the typeface default; use modest tracking for small uppercase labels; avoid aggressive tightening without typographic reason.
- Use tabular numerals for aligned comparison or dynamically changing values that would otherwise jitter.
- Use balanced wrapping for short headings and prettier wrapping for prose as progressive enhancements when they improve the composition.
- Provide sensible fallbacks and prevent font loading from hiding content or causing disruptive shifts.
- Do not use oversized display type merely to make a page look designed.

Check: Can users read comfortably and understand structure without color, containers, or decoration?

## 6. Color

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

## 7. Surfaces and depth

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

## 8. Components

Build consistent, understandable units without unnecessary abstraction or variant complexity.

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
- Give icon-only controls familiar symbols, accessible names, and tooltips where helpful. Use text when an icon would remain ambiguous.
- Provide adequate target size and separation without requiring the visible shape to fill the target.
- Support long labels, wrapping, localization, real data, empty values, and narrow containers.
- Avoid making an entire container clickable when it includes nested controls or links.

Check: Does each component stay understandable, consistent, and stable in every context and state?

## 9. Interaction and motion

Make interactions predictable, responsive, reversible where possible, and appropriate to the input method.

- Keep primary and commonly used actions visible.
- Reveal repetitive secondary or destructive row actions on hover when permanent display would create noise, but also reveal them on focus or selection and provide a touch path such as an overflow menu.
- Never hide the only route to a core task, required information, or unfamiliar interaction behind hover.
- Reserve space for revealed controls or overlay them intentionally so rows and targets do not shift.
- Give every action immediate and proportional feedback near the affected content.
- Preserve user context: avoid unnecessary navigation, scroll jumps, focus loss, and resets.
- Prevent duplicate submissions while pending and keep the interface informative rather than inert.
- Use optimistic updates only when success is likely, reversal is easy, and failure can be reconciled clearly.
- Preserve user input on failure, explain the problem usefully, and offer recovery.
- Prefer undo for common reversible actions. Confirm destructive, costly, or difficult-to-reverse actions with non-obvious consequences.
- Avoid confirmation for low-risk actions merely because it is easy to add.
- Avoid unexpected navigation, autoplay, automatic submission, or changes triggered by hover alone.
- Support mouse, touch, and keyboard; provide alternatives to hover, precision pointing, gestures, and drag-and-drop.
- Manage overlays predictably: place focus appropriately, provide dismissal, return focus to the trigger, and protect unsaved work.

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

## 10. Responsiveness

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

## 11. Accessibility

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

## 12. Polish

Resolve visible roughness and inconsistency rather than adding decoration or pursuing invisible perfection.

- Judge realistic content, data, states, and viewport sizes instead of only the ideal default screen.
- Check alignment, spacing, wrapping, overflow, clipping, truncation, and baseline relationships across repeated elements.
- Verify every relevant default, hover, focus, pressed, selected, disabled, loading, empty, success, and error state.
- Keep icon size, stroke, fill style, and visual language coherent.
- Handle images deliberately: preserve aspect ratio, choose useful crops, provide sufficient resolution, and reserve loading space.

### Truncation

- Treat overflow as a content decision rather than a blanket CSS fix.
- Let meaningful content wrap when the layout can grow.
- Clamp repeated cards or rows when stable rhythm matters.
- Use an ellipsis for a discrete label or value whose omission is expected.
- Use a fade for preview or continuation, not for controls or critical exact values.
- Do not use character counts as a visual substitute for available-space measurement, especially with proportional type.
- Use real character limits only when the content domain requires them.
- Preserve distinguishing content. Middle-truncate paths, identifiers, or filenames when both ends matter; do not silently hide critical statuses, values, or extensions.
- Make complete content available through an appropriate detail, expansion, focus, or hover path rather than hover alone.

### Spatial stability

- Treat accidental layout shift near the pointer, focus, reading position, or active control as a major quality defect.
- Reserve realistic space for media, changing controls, hover actions, validation, loading states, and asynchronous content.
- Make skeletons and placeholders approximate final geometry.
- Avoid inserting late content above the current viewport or focus without preserving position.
- Prefer stable dimensions, overlays, transforms, and opacity feedback when a response need not reflow its surroundings.
- Allow intentional reflow for meaningful expansion, insertion, removal, or content change. Keep the trigger or focal object anchored and animate only when it clarifies where content went.

### Finishing discipline

- Keep terminology, capitalization, punctuation, labels, date/number formats, and tone consistent.
- Remove dead controls, duplicate information, placeholders, unexplained sample data, and obsolete decoration.
- Move recurring one-off values into tokens or shared components only when they reveal a real pattern.
- Test complete interaction paths, including focus, scroll position, errors, recovery, and returning from overlays.
- Prioritize visible and use-affecting issues; do not delay completion for microscopic differences at normal viewing conditions.
- Never let pixel refinement break responsiveness, semantics, accessibility, content resilience, or maintainability.
- Use manual optical correction only when the user explicitly requests it or identifies a visible imbalance.
- Before any optical nudge, correct geometry. Limit adjustment to an asymmetric shape inside a fixed control and normally to 1 CSS pixel. If more than 2 pixels seems necessary, fix the asset, dimensions, typography, or layout.
- Apply an approved correction to the shared component or asset, never to grids, text blocks, group spacing, or general layout.

Check: Does the interface feel finished because rough edges are resolved rather than because more styling was added?

## 13. Restraint

Concentrate attention and character where they matter. Treat restraint as disciplined prioritization, not a mandate for minimalism.

- Give each screen a limited attention budget. When everything uses strong color, scale, contrast, elevation, or motion, nothing remains special.
- Let one or two ideas carry the character rather than applying every available technique.
- Use the simplest treatment that communicates hierarchy, affordance, or state. Add another cue only for distinct information or intentional expression.
- Remove elements, labels, controls, and decoration that repeat what is already clear or do not support the task.
- Avoid ornamental UI furniture: unnecessary cards, dividers, badges, pills, icons, gradients, shadows, and eyebrow labels.
- Reserve noticeable motion for changes that benefit from spatial explanation, emphasis, feedback, or delight.
- Reuse established components and patterns before adding one for a minor variation.
- Keep secondary actions subordinate without making them cryptic, inaccessible, or artificially faint.
- Use sensible defaults and progressive disclosure when controls would compete with the primary task.
- Resolve content, hierarchy, responsiveness, and interaction before polishing low-value details.
- Allow maximal, dense, playful, expressive, and unconventional design when it serves the project. Edit rigorously within that direction instead of neutralizing it.
- Stop when the interface communicates clearly and feels coherent.

Check: Does every prominent choice earn the attention it consumes?

## 14. Slop prevention

Actively resist generation shortcuts that produce plausible but generic, incoherent, or unfinished UI. Treat these as defaults to question, not universal style bans.

- Do not treat giant heroes, centered headlines, gradient text, three-card feature rows, statistic strips, dashboard card grids, sidebars, or top navigation as product requirements.
- Do not invent claims, metrics, testimonials, activity, notifications, categories, or features to fill the composition.
- Use real product content when available and clearly intentional sample data when necessary.
- Remove generic filler copy, redundant subtitles, decorative eyebrows, and instructions that narrate an interface that could be self-explanatory.
- Do not turn every section, datum, action, and status into a card, pill, badge, or bordered container.
- Question gratuitous purple-blue gradients, glows, glass, oversized rounded rectangles, excessive whitespace, enormous type, floating blobs, and universal animation. Use them only when the visual thesis supports them.
- Use icons for recognition or justified space savings, not to decorate every label. Keep one coherent icon family and do not mix arbitrary symbols, emoji, fill styles, and outline styles.
- Preserve existing language, architecture, components, and brand during revisions. Do not substitute a generic redesign or expand scope because rebuilding is easier.
- Make every visible control real. Remove dead buttons, fake filters, unexplained charts, placeholder navigation, and hover effects on static objects.
- Do not add a dependency, abstraction, design system, animation framework, or broad component API for a small visual problem unless the project will benefit.
- Stress realistic content and intermediate widths. Generated layouts often work only with short labels, uniform cards, ideal data, and one screenshot width.
- Before finishing, remove anything borrowed from a generic landing-page or dashboard recipe that cannot be justified by this product's content, task, or direction.

Check: Does the interface feel specifically designed for this product, with every visible element supported by real content, behavior, or intent?
