# Arc Design System

Arc is the source of truth for its design tokens and Figma handoff. Token definitions live in Git and their generated CSS is committed so product implementations and the shared design library use the same decisions.

## Design-system guidance

Read the [design-system documentation](./design-system/README.md) for token architecture, component guidance, accessibility constraints, and the JSON → CSS → Figma maintenance flow. The copy-ready [Figma variable handoff](./design-system/figma/variables.md) accompanies the [Arc Design System Figma library](https://www.figma.com/design/6voYmWnWTpdBTS7f1az0ZU/etaylor.co-Design-System?node-id=0-1&p=f&t=5xVg2WFhFsojL3Td-0).

## Token commands

Run these commands from the repository root:

- `npm run tokens:validate` validates token aliases, policy boundaries, and accessibility rules.
- `npm run tokens:build` regenerates `design-system/tokens/tokens.css` from the JSON sources.
- `npm run tokens:test` runs the token contract and regression tests.
- `npm run tokens:check` runs the complete validation, build, generated-output parity, and test sequence.

Do not edit generated CSS directly. Update the owning JSON token layer, validate and build it, then mirror the approved change in the Figma handoff and library.
