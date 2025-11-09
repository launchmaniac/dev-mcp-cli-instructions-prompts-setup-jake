# GitHub MCP Authentication

## Creating Personal Access Token (PAT)

**1. Navigate to GitHub Token Settings:**
- Login to GitHub
- Go to: https://github.com/settings/tokens/new
- Or: Settings → Developer settings → Personal access tokens → Tokens (classic)

**2. Configure Token:**

**Name:** `Claude Code MCP`

**Expiration:**
- No expiration (most convenient)
- 90 days (more secure, requires renewal)

**Scopes (Required):**
- ✅ `repo` - Full control of private repositories
  - Enables: read files, create/update files, create PRs, manage issues
- ✅ `read:org` - Read org and team membership
  - Enables: access organization repos, see team structure

**Optional Scopes:**
- `workflow` - If you need to manage GitHub Actions
- `gist` - If you need to create/manage gists

**3. Generate and Copy:**
- Click "Generate token"
- **Copy token immediately** (starts with `ghp_`)
- Store securely (won't be shown again)

## Token Security

**DO:**
- Store token in settings.json only
- Keep settings.json in your home directory
- Add settings.json to .gitignore
- Use fine-grained tokens for specific repos (advanced)
- Set expiration dates for production use

**DON'T:**
- Commit token to any repository
- Share token via email/chat/Slack
- Use same token across multiple computers (create separate tokens)
- Store token in plaintext files in repos

## Token Permissions

Your Personal Access Token grants:
- Read access to all repos you can access
- Write access to repos you have push permission
- Create PRs, issues, comments
- Search code across all accessible repos
- Access organization repos (with read:org)

## Revoking Access

**To revoke GitHub MCP access:**

1. Go to: https://github.com/settings/tokens
2. Find "Claude Code MCP" token
3. Click "Delete"
4. Update settings.json (remove or replace token)
5. Restart Claude Code

## Multiple GitHub Accounts

If you have multiple GitHub accounts:

**Option 1 - Switch tokens:**
- Create PAT for each account
- Swap tokens in settings.json as needed
- Restart Claude Code after swap

**Option 2 - Multiple MCP servers:**
```json
{
  "mcpServers": {
    "github-personal": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_personal_token"
      }
    },
    "github-work": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_work_token"
      }
    }
  }
}
```

## Token vs OAuth (gh auth login)

**Personal Access Token (for MCP):**
- Programmatic access
- Specified scopes
- Long-lived credentials
- Required for GitHub MCP

**OAuth (gh auth login):**
- Interactive browser login
- All accessible scopes
- Short-lived sessions
- Used by GitHub CLI

**Both can coexist** - use OAuth for CLI commands, PAT for MCP integration.

## Troubleshooting

**"Bad credentials" error:**
- Token expired → create new token
- Token deleted → check GitHub settings
- Wrong token → verify copy/paste

**"Resource not accessible" error:**
- Missing `repo` scope → regenerate token
- No access to repo → check repo permissions
- Private repo → ensure PAT has private repo access
