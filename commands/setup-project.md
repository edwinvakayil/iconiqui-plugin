---
name: setup-project
description: Initialize shadcn and add the Iconiq @iconiq registry to components.json for this workspace.
---

# Set up Iconiq in this project

1. Check whether `components.json` exists in the workspace root.
2. If missing, run `npx shadcn@latest init` and follow shadcn prompts for the user's React or Next.js stack.
3. Open `components.json` and ensure the Iconiq registry is present under `registries`:

```json
{
  "registries": {
    "@iconiq": "https://iconiqui.com/r/{name}.json"
  }
}
```

4. Preserve existing registry entries — merge, do not replace unrelated keys.
5. Confirm shadcn MCP is enabled (plugin `mcp.json` provides the shadcn server).
6. Tell the user they can now install components with `npx shadcn@latest add @iconiq/<name>` or by asking the agent to add a specific `@iconiq` component.

Docs: https://iconiqui.com/installation
