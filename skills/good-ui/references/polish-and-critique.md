# Polish and critique

Use this reference when resolving finishing details, truncation, layout stability, restraint, agent-generated slop, or reviewing substantial UI work before delivery.

## Contents

- [Polish](#polish)
- [Restraint](#restraint)
- [Slop prevention](#slop-prevention)

## Polish

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
- If meaningful content is clamped, provide a keyboard- and touch-operable expansion or detail view. A tooltip or title attribute may supplement that path but must not be the sole disclosure.

### Spatial stability

- Treat accidental layout shift near the pointer, focus, reading position, or active control as a major quality defect.
- Reserve realistic space for media, changing controls, hover actions, validation, loading states, and asynchronous content.
- Make skeletons and placeholders approximate final geometry.
- Avoid inserting late content above the current viewport or focus without preserving position.
- Prefer stable dimensions, overlays, transforms, and opacity feedback when a response need not reflow its surroundings.
- Allow intentional reflow for meaningful expansion, insertion, removal, or content change. Keep the trigger or focal object anchored and animate only when it clarifies where content went.

### Finishing discipline

- Keep terminology, capitalization, punctuation, labels, date/number formats, and tone consistent.
- Humanize generated labels and source names instead of exposing concatenated domains, machine casing, or raw identifiers without purpose.
- Remove dead controls, duplicate information, placeholders, unexplained sample data, and obsolete decoration.
- Do not synthesize factual-looking metadata merely to preserve a row or card anatomy. Omit it, request it, or label a defensible calculation explicitly as an estimate.
- Move recurring one-off values into tokens or shared components only when they reveal a real pattern.
- Test complete interaction paths, including focus, scroll position, errors, recovery, and returning from overlays.
- Prioritize visible and use-affecting issues; do not delay completion for microscopic differences at normal viewing conditions.
- Never let pixel refinement break responsiveness, semantics, accessibility, content resilience, or maintainability.
- Use manual optical correction only when the user explicitly requests it or identifies a visible imbalance.
- Before any optical nudge, correct geometry. Limit adjustment to an asymmetric shape inside a fixed control and normally to 1 CSS pixel. If more than 2 pixels seems necessary, fix the asset, dimensions, typography, or layout.
- Apply an approved correction to the shared component or asset, never to grids, text blocks, group spacing, or general layout.

### Mandatory rendered review

- Render substantial UI work at representative wide, intermediate, and narrow sizes. Inspect the pixels; do not treat the existence of responsive CSS or component states as evidence that the composition works.
- Check the first viewport: does useful product content dominate, or has low-value atmosphere pushed the task away?
- Check shared edges, baseline relationships, content widths, density, wrapping, and the distance between related controls. Correct arbitrary offsets and dead zones.
- Check control affordances at normal viewing size. Tiny icons, faint labels, ambiguous status markers, and invisible input boundaries may be technically present but visually incompetent.
- Check whether the visual direction is improving the product or performing “design” around it. Remove theatrical copy, scale, spacing, and decoration that do not help use.
- Make at least one deliberate correction pass after seeing the rendered result. Do not ship the first coherent-looking composition.

### Mandatory interaction review

- Exercise every visible control and remove dead or placeholder affordances.
- Test malformed and boundary input, long-content recovery, repeated destructive actions and undo, and keyboard-only operation across state mutations.
- Verify that focus, scroll position, and spatial context survive filtering, rerendering, insertion, removal, and overlay dismissal.
- Verify that dynamic announcements are concise and that factual-looking content or metadata is truthful.

Check: Does the interface feel finished because rough edges are resolved rather than because more styling was added?

## Restraint

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

## Slop prevention

Actively resist generation shortcuts that produce plausible but generic, incoherent, or unfinished UI. Treat these as defaults to question, not universal style bans.

- Do not treat giant heroes, centered headlines, gradient text, three-card feature rows, statistic strips, dashboard card grids, sidebars, or top navigation as product requirements.
- Do not invent claims, metrics, testimonials, activity, notifications, categories, or features to fill the composition.
- Use real product content when available and clearly intentional sample data when necessary.
- Remove generic filler copy, redundant subtitles, decorative eyebrows, and instructions that narrate an interface that could be self-explanatory.
- Do not turn every section, datum, action, and status into a card, pill, badge, or bordered container.
- Question gratuitous purple-blue gradients, glows, glass, oversized rounded rectangles, excessive whitespace, enormous type, floating blobs, and universal animation. Use them only when the visual thesis supports them.
- Question the current editorial-agent style bundle with equal rigor: paper-toned backgrounds, a giant serif statement split across lines, one italic accent word, rust or orange highlights, tiny uppercase metadata, decorative dates, colored punctuation in a wordmark, sparse divider rows, and large areas of cultivated emptiness. Any one may work; combining them by reflex is not product-specific design.
- Do not translate a product category into its most literal visual genre by default: reading into a magazine spread, finance into glassy charts, developer tools into terminal theater, or creative work into floating gradient blobs.
- Do not turn a utility into a landing page. A recurring-use application rarely needs a persistent hero or philosophical tagline above its controls and content.
- Do not let art direction excuse weak alignment, low information density, tiny controls, ambiguous affordances, crude labels, or unfinished interaction behavior.
- Use icons for recognition or justified space savings, not to decorate every label. Keep one coherent icon family and do not mix arbitrary symbols, emoji, fill styles, and outline styles.
- Preserve existing language, architecture, components, and brand during revisions. Do not substitute a generic redesign or expand scope because rebuilding is easier.
- Make every visible control real. Remove dead buttons, fake filters, unexplained charts, placeholder navigation, and hover effects on static objects.
- Do not add a dependency, abstraction, design system, animation framework, or broad component API for a small visual problem unless the project will benefit.
- Stress realistic content and intermediate widths. Generated layouts often work only with short labels, uniform cards, ideal data, and one screenshot width.
- Before finishing, remove anything borrowed from a generic landing-page or dashboard recipe that cannot be justified by this product's content, task, or direction.

Check: Does the interface feel specifically designed for this product, with every visible element supported by real content, behavior, or intent?
