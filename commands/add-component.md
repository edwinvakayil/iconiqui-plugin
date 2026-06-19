---
name: add-component
description: Install an Iconiq UI component from the @iconiq registry into the current project and wire it into the requested page or feature.
---

# Add an Iconiq component

1. Confirm `components.json` includes the `@iconiq` registry (`https://iconiqui.com/r/{name}.json`). If not, run setup first.
2. Identify the component slug from the user request or https://iconiqui.com.
3. If both Base UI and Radix UI variants exist (`b-` and `r-` prefixes), confirm which variant to use.
4. Install with shadcn MCP or:

```bash
npx shadcn@latest add @iconiq/<slug>
```

5. Import the generated component using the project's path alias (commonly `@/components/ui/<slug>`).
6. Integrate into the target file with props and layout matching Iconiq docs.
7. Run lint or typecheck if the project has them configured.

Example slugs: `b-button`, `accordion`, `combobox`, `status-dot`, `calendar`.

Docs: https://iconiqui.com
