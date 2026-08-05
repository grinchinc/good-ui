# Composition and visual direction

Use this reference when establishing or revising intentionality, application composition, hierarchy, layout, spacing, or typography.

## Contents

- [Intentionality](#intentionality)
- [Hierarchy](#hierarchy)
- [Layout](#layout)
- [Spacing](#spacing)
- [Typography](#typography)

## Intentionality

Make the UI feel guided by a coherent point of view rather than assembled from individually reasonable defaults. Keep that point of view in service of the product.

- Begin with the product's recurring task, audience, content, existing brand, and desired tone.
- Let those constraints inform typography, color, density, shape, imagery, and motion. A visual thesis may be subtle and structural; it does not need a slogan, literal theme, or signature effect.
- Respect existing brand and project conventions. Extend them rather than casually replacing them.
- Avoid unconscious defaults and fashionable clichés, especially interchangeable SaaS layouts.
- Do not equate good design with minimal, neutral, spacious, or corporate. Expressive, dense, playful, and unconventional interfaces can be highly competent.
- Repeat a small number of visual ideas so the experience feels authored and cohesive.
- Make decorative choices reinforce identity, hierarchy, meaning, or delight.
- Do not invent interface copy, metadata, or decorative sections merely to express the visual direction.
- Correct accidental inconsistency without sanding away deliberate character.
- Prefer a clear direction over a timid mixture of visual styles.

### Application versus marketing composition

- Identify whether the surface is an operational application, content experience, marketing page, or onboarding moment before choosing its composition.
- Let an operational interface open on the working surface: the recurring task, current state, and useful content. Persistent heroes, manifestos, taglines, decorative dates, and promotional statements require a current user need.
- Express identity through the working interface itself—type, color, density, rhythm, controls, and content treatment—before adding a separate atmospheric section.
- Make frequently used tools less ceremonial after the first visit. Introductory material that helps once should not permanently dominate every session.
- If non-functional copy or decoration consumes more of the initial viewport than the primary task, remove, reduce, or relocate it unless the product explicitly depends on that experience.

Check: Can someone explain why this interface looks this way beyond “it looks modern”?

## Hierarchy

Make importance, relationships, and the intended path apparent before the user reads every word.

- Give each screen or region one clear focal point and primary purpose.
- Make the most important information and action visually dominant; do not let several elements compete for first attention.
- Make prominence proportional to utility, frequency, and consequence. Large display copy is not justified merely because it creates drama.
- Ensure the primary product surface—not a decorative explanation of the product—wins the initial attention hierarchy in recurring-use applications.
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

## Layout

Give content a clear spatial logic that feels stable, connected, and easy to scan.

- Establish an underlying grid or small set of alignment lines. Avoid independently positioned elements.
- Use as few alignment axes as the composition reasonably permits.
- Align related elements precisely; use asymmetry deliberately rather than accidentally.
- Align global chrome, primary content, toolbars, and repeated rows to a coherent set of shared edges unless an offset communicates a real relationship.
- Choose widths for the material. Prose, forms, data tables, and immersive media do not need the same container.
- Constrain long-form text to a comfortable reading measure.
- Do not make every section full-width because the viewport allows it.
- Treat whitespace as composition, but match density to the task; more space is not automatically better.
- Do not use empty space to manufacture importance for low-value copy. On large screens, keep related controls and content visually connected rather than pushing them apart because room exists.
- Give the initial viewport a useful amount of the product. For recurring tools, users should not need to pass a ceremonial header before reaching the working surface.
- Prefer natural flow and flexible constraints over brittle fixed positioning.
- Use centered composition for short, focused material. Prefer left alignment for scanning and complex information.
- Give prominent elements enough surrounding space to carry their visual weight.
- Balance the whole screen, not only each component in isolation.
- Test with real content lengths rather than placeholder-perfect copy.

Check: Does every element have a clear spatial relationship to the elements around it?

## Spacing

Use space to create rhythm, communicate relationships, and establish an appropriate density.

- Use a deliberate scale or small family of recurring values instead of arbitrary gaps.
- Keep space within a group smaller than space between groups, and group spacing smaller than major section spacing.
- Keep repeated components and repeated relationships spatially consistent.
- Choose component padding from its content and intended density rather than applying one universal value.
- Make horizontal and vertical padding feel balanced without requiring numeric equality.
- Avoid blanket uniformity where every gap is identical and uncontrolled variety where every gap is unique.
- Match density to context. Productivity interfaces may need compact efficiency; focused or expressive experiences may need more breathing room.
- Match row and section height to interaction frequency and information value. Repeated utility content should not become oversized merely to make the page feel luxurious.
- Preserve adequate target size and readability even in compact layouts.
- Treat unexpected one-off spacing values as a signal to inspect the underlying structure.
- Prefer shared spacing tokens once a recurring relationship is established.

Check: Can the spacing alone reveal which things belong together and which begin a new idea?

## Typography

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
- Do not treat genre as a typography preset. A reading product does not automatically require a newspaper-like serif, italic accent line, uppercase metadata, or oversized editorial headline; choose these only when the whole product benefits.
- Keep body tracking near the typeface default; use modest tracking for small uppercase labels; avoid aggressive tightening without typographic reason.
- Use tabular numerals for aligned comparison or dynamically changing values that would otherwise jitter.
- Use balanced wrapping for short headings and prettier wrapping for prose as progressive enhancements when they improve the composition.
- Provide sensible fallbacks and prevent font loading from hiding content or causing disruptive shifts.
- Do not use oversized display type merely to make a page look designed.

Check: Can users read comfortably and understand structure without color, containers, or decoration?
