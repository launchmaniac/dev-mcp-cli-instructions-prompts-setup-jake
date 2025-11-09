# GitHub MCP Installation

## Prerequisites

- Node.js installed (npm command available)
- GitHub account
- Personal Access Token (will create during setup)

## Installation Steps

**1. Install GitHub MCP server globally:**

```bash
npm install -g @modelcontextprotocol/server-github
```

**2. Create GitHub Personal Access Token:**

- Go to: https://github.com/settings/tokens/new
- Token name: "Claude Code MCP"
- Expiration: No expiration (or 90 days for security)
- Select scopes:
  - ✅ `repo` (Full control of private repositories)
  - ✅ `read:org` (Read org and team membership)
- Click "Generate token"
- **Copy the token immediately** (you won't see it again)

**3. Configure Claude Code:**

Open or create: `~/.claude/settings.json` (Windows: `C:\Users\[Your Name]\.claude\settings.json`)

Add to `mcpServers` section:

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

## Verification

In Claude Code, try:
```
List all my GitHub repositories
```

If configured correctly, Claude will show your repos.

## Troubleshooting

**Error: "command not found: npx"**
- Install Node.js: https://nodejs.org/

**Error: "Bad credentials"**
- Token expired → create new token
- Token copied incorrectly → check for extra spaces
- Missing `repo` scope → regenerate with correct scopes

**No GitHub tools available**
- Check settings.json syntax (valid JSON)
- Restart Claude Code completely
- Check Claude Code logs for errors

## Security Note

**NEVER commit your Personal Access Token to GitHub.**

Add to .gitignore:
```
settings.json
.claude/settings.json
```

## Documentation

Full MCP documentation: https://github.com/modelcontextprotocol/servers/tree/main/src/github
