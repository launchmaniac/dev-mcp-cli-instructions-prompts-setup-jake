# ClickUp MCP Installation

## Prerequisites

- Node.js installed (npm command available)
- ClickUp workspace with API access

## Installation Steps

**1. Install ClickUp MCP server globally:**

```bash
npm install -g @modelcontextprotocol/server-clickup
```

**2. Get your ClickUp API token:**

- Go to: https://app.clickup.com/settings/apps
- Click "Generate" under API Token section
- Copy the token (you won't see it again)

**3. Configure Claude Code:**

Open or create: `~/.claude/settings.json` (Windows: `C:\Users\[Your Name]\.claude\settings.json`)

Add to `mcpServers` section:

```json
{
  "mcpServers": {
    "clickup": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-clickup"],
      "env": {
        "CLICKUP_API_TOKEN": "your_api_token_here"
      }
    }
  }
}
```

**4. Restart Claude Code**

## Verification

In Claude Code, try:
```
Can you search for tasks in ClickUp assigned to me?
```

If configured correctly, Claude will access your ClickUp workspace.

## Troubleshooting

**Error: "command not found: npx"**
- Install Node.js: https://nodejs.org/

**Error: "Invalid API token"**
- Regenerate token in ClickUp settings
- Ensure no extra spaces when copying token

**No ClickUp tools available**
- Check settings.json syntax (valid JSON)
- Restart Claude Code completely
- Check Claude Code logs for errors

## Documentation

Full MCP documentation: https://github.com/modelcontextprotocol/servers/tree/main/src/clickup
