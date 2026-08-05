# Good UI

A portable agent skill for designing polished, intentional, resilient interfaces without generic UI slop.

Good UI is a principle-driven design judgment layer for agents creating or revising apps and websites. It covers hierarchy, layout, spacing, typography, semantic color systems, surfaces, components, interaction states, motion, responsiveness, accessibility, polish, restraint, and common agent-generated failure modes without imposing one visual style.

## Install

```bash
npx skills add grinchinc/good-ui --skill good-ui
```

Install globally for Codex without prompts:

```bash
npx skills add grinchinc/good-ui --skill good-ui --agent codex --global --yes
```

## Structure

- `skills/good-ui/SKILL.md` is the behavioral core: sequence of attention, decision priorities, requirements, strong defaults, failure modes, reference routing, and the completion gate.
- `skills/good-ui/references/composition.md` covers visual direction, hierarchy, layout, spacing, and typography.
- `skills/good-ui/references/system-and-components.md` covers color systems, surfaces, depth, components, and reusable interaction primitives.
- `skills/good-ui/references/interaction-and-responsiveness.md` covers states, feedback, motion, responsive behavior, and accessibility.
- `skills/good-ui/references/polish-and-critique.md` covers truncation, spatial stability, finishing discipline, restraint, slop prevention, and final review.


## License

MIT
