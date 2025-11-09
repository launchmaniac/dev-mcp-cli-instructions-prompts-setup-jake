# ClickUp MCP Authentication

## Getting Your API Token

**1. Navigate to ClickUp Settings:**
- Login to ClickUp: https://app.clickup.com
- Click your avatar (bottom left)
- Select "Settings"

**2. Generate API Token:**
- Go to "Apps" tab
- Scroll to "API Token" section
- Click "Generate" (or "Regenerate" if you had one before)
- **Copy the token immediately** (won't be shown again)

## Token Security

**DO:**
- Store token in settings.json only
- Keep settings.json in your home directory (not in git repos)
- Use different tokens for different computers
- Regenerate token if compromised

**DON'T:**
- Commit settings.json to GitHub
- Share token via email/chat
- Use same token across team members

## Token Permissions

Your API token has access to:
- All workspaces you're a member of
- All tasks, spaces, folders, lists you can access
- Create/update/delete permissions match your user role

**Workspace ID auto-detection:** MCP automatically uses your default workspace. Override with `workspace_id` parameter if needed.

## Revoking Access

**To revoke ClickUp MCP access:**

1. Go to ClickUp Settings → Apps → API Token
2. Click "Regenerate" (invalidates old token)
3. Update settings.json with new token (or remove to disable)
4. Restart Claude Code

## Multiple Workspaces

If you have multiple ClickUp workspaces:

1. MCP defaults to your primary workspace
2. Override by passing `workspace_id` in tool calls
3. Find workspace ID in ClickUp URL: `https://app.clickup.com/[workspace_id]/home`

## Troubleshooting

**"Unauthorized" errors:**
- Token expired or revoked → regenerate
- Token copied incorrectly → check for extra spaces

**"Workspace not found":**
- Verify workspace_id in URL
- Ensure you're a member of the workspace
