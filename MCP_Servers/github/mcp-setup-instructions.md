# GitHub MCP Setup Instructions

## Best Practice Reference

**ClickUp MCP setup (HTTP transport):**
```bash
claude mcp add --transport http clickup https://mcp.clickup.com/mcp
```

## GitHub MCP Setup Options

### Option 1: NPM Package (Recommended)

GitHub MCP uses a local npm package, not HTTP transport like ClickUp.

**1. Install GitHub MCP package:**
```bash
npm install -g @modelcontextprotocol/server-github
```

**2. Get Personal Access Token:**
- Go to: https://github.com/settings/tokens/new
- Token name: "Claude Code MCP"
- Scopes: `repo`, `read:org`
- Generate and copy token

**3. Add to Claude Code:**
```bash
claude mcp add github
```

**Configure when prompted:**
- Command: `npx`
- Args: `-y @modelcontextprotocol/server-github`
- Environment variables:
  - `GITHUB_PERSONAL_ACCESS_TOKEN`: [paste your token]

**Alternative manual config in `~/.claude/settings.json`:**
```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_your_token_here"
      }
    }
  }
}
```

**4. Restart Claude Code**

### Option 2: Check for HTTP Transport (Future)

If GitHub releases HTTP MCP endpoint like ClickUp:

```bash
claude mcp add --transport http github https://[github-mcp-endpoint]
```

*Note: As of Nov 2025, GitHub does not provide HTTP MCP transport. Use npm package method.*

## Verification

**Test GitHub MCP:**
```
List all my GitHub repositories
```

**Expected:** Claude shows your repos from GitHub API.

## Comparison: ClickUp vs GitHub MCP

| Feature | ClickUp MCP | GitHub MCP |
|---------|-------------|------------|
| **Transport** | HTTP (hosted service) | NPM (local process) |
| **Setup** | One command | Install package + configure |
| **Token** | ClickUp API token | GitHub Personal Access Token |
| **Command** | `claude mcp add --transport http` | `claude mcp add` (stdio) |
| **Endpoint** | `https://mcp.clickup.com/mcp` | Local npx process |

## Why Different Approaches?

**ClickUp:**
- Hosts MCP server at `mcp.clickup.com`
- HTTP transport = lightweight client
- No local installation needed

**GitHub:**
- MCP server runs locally via npm
- Stdio transport = communicates via stdin/stdout
- Requires Node.js installed

## Best Practice Pattern

**If HTTP endpoint available (like ClickUp):**
```bash
claude mcp add --transport http [service-name] [endpoint-url]
```

**If local server required (like GitHub):**
```bash
npm install -g @modelcontextprotocol/server-[service-name]
claude mcp add [service-name]
# Configure command, args, env variables
```

## Troubleshooting

**"GitHub MCP not working":**
1. Verify npm package installed: `npm list -g @modelcontextprotocol/server-github`
2. Check token has `repo` scope
3. Restart Claude Code
4. Check settings.json syntax (valid JSON)

**"Command not found: npx":**
- Install Node.js: https://nodejs.org/

**"Bad credentials":**
- Regenerate GitHub Personal Access Token
- Ensure `repo` scope selected
- Update token in settings.json
