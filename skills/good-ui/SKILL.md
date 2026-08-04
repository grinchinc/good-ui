---
name: good-ui
description: Apply broadly useful visual and interaction design fundamentals when creating, implementing, reviewing, or revising apps and websites, especially Bash.tv projects. Use for UI layout, hierarchy, spacing, typography, color systems, surfaces, components, states, motion, responsiveness, accessibility, polish, and preventing generic agent-generated design slop. Preserve the project's brand and tone rather than imposing a fixed aesthetic.
---

# Good UI

Use this skill as a design-judgment layer, not as a visual style or a rigid workflow. Make the interface feel intentional, competent, and specific to its product while preserving existing brand character and the user's direction. Establish functional competence before adding conspicuous art direction.

## Core rules — do not ignore

1. **Design for the task, not a concept.** Derive visual decisions from the product, audience, content, and existing brand. Product-specific design should improve use; it does not require a literal theme, manifesto, or conspicuous visual thesis.
2. **Make the working surface primary.** In application UI, put the recurring task and useful content ahead of promotional composition. Do not wrap a tool in a landing-page hero unless that material serves a real, current user need.
3. **Establish competence before expression.** Resolve alignment, density, typography, control affordance, content quality, state behavior, and responsiveness before spending attention on art direction.
4. **Make hierarchy proportional.** Give every screen a clear focal point and action priority, but size each element according to its actual utility and frequency. Decorative or explanatory copy must not overpower the product.
5. **Prefer structure over enclosure.** Communicate grouping with alignment, proximity, and typography before reaching for cards, borders, dividers, backgrounds, or nested containers. Avoid container slop and line slop.
6. **Use a coherent system.** Reuse a small spacing scale, semantic type styles, consistent shape language, and a color token chain of palette → semantic roles → components. Build color relationships in OKLCH and evaluate readable pairs with APCA.
7. **Make typography carry its share.** Choose readable type, sensible measures and line heights, a small number of clearly distinct levels, and wrapping that survives real content. Do not decorate every heading with an eyebrow label.
8. **Keep the layout stable and resilient.** Align precisely, reserve space for asynchronous or changing content, avoid careless layout shift, and test realistic data, long labels, empty states, and intermediate viewport sizes.
9. **Make components complete.** Use the correct semantic element and implement every relevant state: default, hover where available, pressed, focus-visible, disabled, selected, loading, empty, success, and error. Do not ship fake or dead controls.
10. **Reuse behavior; own the presentation.** Inspect the existing stack before building primitives. Prefer native semantics and proven components for difficult behavior, but skin them to the product rather than accepting accidental browser chrome or a library's demo aesthetic.
11. **Preserve capability across inputs and sizes.** Keep core tasks usable across mouse, keyboard, touch, narrow screens, zoom, and localization. Adapt the composition instead of merely shrinking or stacking it.
12. **Make interaction feedback proportional.** Keep primary actions visible, disclose repetitive secondary actions thoughtfully, preserve user context, and make outcomes and recovery clear. Use motion to explain change—not to decorate everything—and choose deliberate easing instead of mechanical linear motion for ordinary state changes.
13. **Build practical accessibility in from the start.** Favor semantic HTML, labels, keyboard operation, visible focus, usable contrast, and reduced-motion support. Calibrate rigor to the project's reach and stakes; avoid both severe preventable barriers and accessibility theater.
14. **Spend attention deliberately.** Strong color, scale, motion, elevation, and decoration are limited resources. Let a few ideas carry the character and remove treatments that do not add meaning or useful expression.
15. **Reject agent slop.** Do not invent content or features to fill a composition, overuse cards/pills/gradients/glass/huge type, mix icon languages, or swap one generic style bundle for another. Every visible element must be justified by real content, behavior, or intent.
16. **Inspect the rendered result.** Do not mistake implemented CSS, component coverage, or a coherent theme for a competent interface. Render substantial work at representative sizes, inspect the actual composition, and correct visible problems before delivery.

## Use the detailed guidance

Read [references/fundamentals.md](references/fundamentals.md) before designing a new app or page, performing a broad visual revision, establishing system-level styles, or conducting a comprehensive UI review.

For a small isolated change, apply the core rules and consult only the relevant section of the reference. Treat the reference as strong defaults with context-sensitive exceptions, not as a checklist that forces every project toward the same aesthetic.

Honor explicit user direction and established project conventions. When breaking a guideline, do so because the product benefits—not because the implementation shortcut is convenient.

Do not apply manual optical nudges unless the user explicitly requests pixel-level or optical refinement, or identifies a specific visible imbalance. Fix geometry, assets, typography, and layout first.
