# Good UI

A portable agent skill for designing polished, intentional, resilient interfaces without generic UI slop.

Good UI is a principle-driven design judgment layer for agents creating or revising apps and websites. It covers hierarchy, layout, spacing, typography, semantic color systems, surfaces, components, interaction states, motion, responsiveness, accessibility, polish, restraint, and common agent-generated failure modes without imposing one visual style.

## Install

```bash
npx skills add grinchinc/good-ui --skill good-ui
```

Install the more opinionated personal overlay:

```bash
npx skills add grinchinc/good-ui --skill good-ui-bobby
```

Install globally for Codex without prompts:

```bash
npx skills add grinchinc/good-ui --skill good-ui --agent codex --global --yes
```

Install the personal overlay globally for Codex:

```bash
npx skills add grinchinc/good-ui --skill good-ui-bobby --agent codex --global --yes
```

## Structure

- `skills/good-ui/SKILL.md` contains the concise core rules that should always be applied.
- `skills/good-ui/references/` contains task-routed guidance for composition, systems/components, interaction/responsiveness, and polish/critique.
- `skills/good-ui-bobby/SKILL.md` adds personal defaults for spacing, interaction, motion, components, project workflow, and in-product exploration.

## License

MIT
