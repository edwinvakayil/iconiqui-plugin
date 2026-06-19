# Iconiq UI — Cursor Plugin

Cursor plugin for [Iconiq UI](https://iconiqui.com): install editable shadcn registry components with rules, skills, MCP, commands, and an agent.

## Included

| Component | Path | Purpose |
|-----------|------|---------|
| Rules | `rules/iconiq-components.mdc` | Always-on guidance for `@iconiq` installs |
| Skill | `skills/iconiq/SKILL.md` | Install and integrate Iconiq components |
| Agent | `agents/component-assistant.md` | Component picker and integration helper |
| Commands | `commands/` | `setup-project`, `add-component` |
| MCP | `mcp.json` | shadcn MCP server for registry installs |

## Quick start

1. Install or link this plugin in Cursor.
2. Enable the **shadcn** MCP server from plugin settings.
3. In a shadcn-ready React/Next.js project, run the **setup-project** command (or ask the agent to add the registry).
4. Install components:

```bash
npx shadcn@latest add @iconiq/b-button
```

Or prompt: *"Add the @iconiq/accordion component to this page."*

## Registry configuration

Add to `components.json`:

```json
{
  "registries": {
    "@iconiq": "https://iconiqui.com/r/{name}.json"
  }
}
```

--- 
Built by [Edwin Vakayil](https://github.com/edwinvakayil) for [Iconiq UI](https://iconiqui.com).