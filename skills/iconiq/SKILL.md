---
name: iconiq
description: Install and integrate Iconiq UI (@iconiq) shadcn registry components into React or Next.js projects. Use when adding Iconiq components, configuring components.json, running shadcn add, or building UI with iconiqui.com components.
---

# Iconiq UI

[iconiqui.com](https://iconiqui.com) — editable shadcn/ui components with subtle motion. Install with `npx shadcn@latest add @iconiq/<name>`.

## When to use

- User asks to add, install, or use an Iconiq component
- Project needs the `@iconiq` registry in `components.json`
- Choosing between Base UI and Radix UI variants
- Wiring installed components into pages or features
- Troubleshooting shadcn or MCP installs for Iconiq

## Prerequisites

1. React or Next.js app with shadcn initialized (`components.json` present).
2. Iconiq registry in `components.json`:

```json
{
  "registries": {
    "@iconiq": "https://iconiqui.com/r/{name}.json"
  }
}
```

3. shadcn MCP enabled (this plugin ships `mcp.json` with the shadcn server) **or** use the CLI directly.

If setup is incomplete, run the **setup-project** command flow or `npx shadcn@latest init`, then add the registry.

## Install a component

```bash
npx shadcn@latest add @iconiq/b-button
npx shadcn@latest add @iconiq/accordion
```

With MCP connected, prompt examples:

- Add the `@iconiq/b-button` component to this page.
- Install `@iconiq/accordion` and keep the generated files editable.
- Show available components in the iconiq registry.

Direct registry URL (alternative):

```bash
npx shadcn@latest add https://iconiqui.com/r/b-button.json
```

## Base UI vs Radix UI

| Variant | Prefix | Example | Notes |
|---------|--------|---------|-------|
| Base UI | `b-` | `@iconiq/b-button` | Built on Base UI primitives |
| Radix UI | `r-` | `@iconiq/r-accordion` | Built on Radix primitives |
| Single variant | none | `@iconiq/status-dot` | Only one implementation exists |

When both exist, ask which variant the user prefers or match the stack already used in the project.

## After install

1. Import from the path shadcn generated (usually `@/components/ui/<slug>`).
2. Read the component docs at `https://iconiqui.com/<section>/<slug>` for props and examples.
3. Customize the local source file — do not treat Iconiq as an opaque npm package.
4. If `@iconiq/iconiq-theme` was installed, keep it for token-driven styling.

## Discover components

- Browse https://iconiqui.com
- Registry index: https://iconiqui.com/r/registry.json
- MCP: ask the shadcn server to list registry items after `@iconiq` is configured

## Troubleshooting

| Issue | Fix |
|-------|-----|
| Unknown registry `@iconiq` | Add registry URL to `components.json` |
| `components.json` missing | Run `npx shadcn@latest init` |
| MCP not listing components | Enable shadcn MCP in Cursor settings; restart if needed |
| Wrong variant installed | Remove generated files and reinstall the `b-` or `r-` slug |

## References

- Installation: https://iconiqui.com/installation
- MCP setup: https://iconiqui.com/mcp
