---
name: good-ui
description: Apply broadly useful visual and interaction design fundamentals when creating, implementing, reviewing, or revising apps and websites, especially Bash.tv projects. Use for UI layout, hierarchy, spacing, typography, color systems, surfaces, components, states, motion, responsiveness, accessibility, polish, and preventing generic agent-generated design slop. Preserve the project's brand and tone rather than imposing a fixed aesthetic.
---

# Good UI

Use this skill as a design-judgment layer, not as a visual style or a rigid workflow. Make the interface feel intentional, competent, and specific to its product while preserving existing brand character and the user's direction.

## Core rules — do not ignore

1. **Design for this product.** Derive the visual direction from the product, audience, content, and existing brand. Do not fall back to generic SaaS layouts or fashionable agent defaults.
2. **Make hierarchy unmistakable.** Give every screen a clear focal point, primary purpose, and action priority. Use size, weight, contrast, position, and space together.
3. **Prefer structure over enclosure.** Communicate grouping with alignment, proximity, and typography before reaching for cards, borders, dividers, backgrounds, or nested containers. Avoid container slop and line slop.
4. **Use a coherent system.** Reuse a small spacing scale, semantic type styles, consistent shape language, and a color token chain of palette → semantic roles → components. Build color relationships in OKLCH and evaluate readable pairs with APCA.
5. **Make typography carry its share.** Choose readable type, sensible measures and line heights, a small number of clearly distinct levels, and wrapping that survives real content. Do not decorate every heading with an eyebrow label.
6. **Keep the layout stable and resilient.** Align precisely, reserve space for asynchronous or changing content, avoid careless layout shift, and test realistic data, long labels, empty states, and intermediate viewport sizes.
7. **Make components complete.** Use the correct semantic element and implement every relevant state: default, hover where available, pressed, focus-visible, disabled, selected, loading, empty, success, and error. Do not ship fake or dead controls.
8. **Preserve capability across inputs and sizes.** Keep core tasks usable across mouse, keyboard, touch, narrow screens, zoom, and localization. Adapt the composition instead of merely shrinking or stacking it.
9. **Make interaction feedback proportional.** Keep primary actions visible, disclose repetitive secondary actions thoughtfully, preserve user context, and make outcomes and recovery clear. Use motion to explain change—not to decorate everything—and choose deliberate easing instead of mechanical linear motion for ordinary state changes.
10. **Build practical accessibility in from the start.** Favor semantic HTML, labels, keyboard operation, visible focus, usable contrast, and reduced-motion support. Calibrate rigor to the project's reach and stakes; avoid both severe preventable barriers and accessibility theater.
11. **Spend attention deliberately.** Strong color, scale, motion, elevation, and decoration are limited resources. Let a few ideas carry the character and remove treatments that do not add meaning or useful expression.
12. **Reject agent slop.** Do not invent content or features to fill a composition, overuse cards/pills/gradients/glass/huge type, mix icon languages, or replace a coherent existing product with a generic redesign. Every visible element must be justified by real content, behavior, or intent.

## Use the detailed guidance

Read [references/fundamentals.md](references/fundamentals.md) before designing a new app or page, performing a broad visual revision, establishing system-level styles, or conducting a comprehensive UI review.

For a small isolated change, apply the core rules and consult only the relevant section of the reference. Treat the reference as strong defaults with context-sensitive exceptions, not as a checklist that forces every project toward the same aesthetic.

Honor explicit user direction and established project conventions. When breaking a guideline, do so because the product benefits—not because the implementation shortcut is convenient.

Do not apply manual optical nudges unless the user explicitly requests pixel-level or optical refinement, or identifies a specific visible imbalance. Fix geometry, assets, typography, and layout first.
