# Paramify Plugin for Claude Code

Connect Claude Code to your Paramify workspace via the Model Context Protocol (MCP).

## Prerequisites

- [Claude Code](https://claude.ai/code)
- An active Paramify workspace with MCP enabled
- Your Paramify MCP server URL and API key (see [Before you install](#before-you-install))

## Before you install

You will need two values from your Paramify workspace:

| Value              | Where to find it                     |
| ------------------ | ------------------------------------ |
| **MCP server URL** | Workspace Settings → Licensing → MCP |
| **API key**        | Workspace Settings → API Keys        |

Keep these handy — Claude Code will prompt you for them during installation.

## Install

Run the following commands inside Claude Code (the `/` commands are Claude Code slash commands, not shell commands):

**Step 1 — Add the Paramify marketplace:**

```
/plugin marketplace add paramify/paramify-plugin
```

**Step 2 — Install the plugin:**

```
/plugin install paramify-plugin@paramify
```

Claude Code will prompt you for your MCP server URL and API key. Enter the values you gathered above.

## Verify the installation

After installation you will have to reload your plugins:

```
/reload-plugins
```

View your list of MCP servers and confirm the Paramify MCP server is connected:

```
/mcp
```

You should see `plugin:paramify-plugin:paramify` listed as a connected server. You can then ask Claude about your workspace — for example:

> "List all my Programs in Paramify."

## Update

To update to the latest version:

```
/plugin update paramify-plugin@paramify
```

## Uninstall

```
/plugin uninstall paramify-plugin@paramify
```

## Configuration reference

The plugin exposes two required configuration values set at install time:

| Field        | Description                                           |
| ------------ | ----------------------------------------------------- |
| `server_url` | The HTTP(S) URL for the Paramify MCP server endpoint  |
| `api_key`    | A Paramify API key. Stored as a sensitive credential. |

To update these values after installation, uninstall and reinstall the plugin.
