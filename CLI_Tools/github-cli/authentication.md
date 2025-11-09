# GitHub CLI Authentication

## Initial Authentication

**Run once per computer:**

```bash
gh auth login
```

**Interactive prompts:**

1. **Where do you use GitHub?**
   → Select: `GitHub.com`

2. **What is your preferred protocol for Git operations?**
   → Select: `HTTPS` (recommended)
   → Alternative: `SSH` (if you have SSH keys configured)

3. **Authenticate Git with your GitHub credentials?**
   → Select: `Yes` (enables git push/pull without passwords)

4. **How would you like to authenticate?**
   → Select: `Login with a web browser` (easiest)
   → Alternative: `Paste an authentication token` (if you have PAT)

5. **Copy one-time code**
   → Example: `5812-8133`
   → Press Enter

6. **Browser opens automatically**
   → Paste code
   → Click "Authorize GitHub CLI"

7. **Success message**
   → `✓ Authentication complete`
   → `✓ Logged in as [username]`

## Checking Authentication Status

**Verify you're logged in:**
```bash
gh auth status
```

**Expected output:**
```
github.com
  ✓ Logged in to github.com as launchmaniac (oauth_token)
  ✓ Git operations for github.com configured to use https protocol.
  ✓ Token: *******************
```

## Refreshing Credentials

**If credentials expire or need refresh:**
```bash
gh auth refresh
```

Follow same prompts as initial login.

## Logging Out

**To logout:**
```bash
gh auth logout
```

**Confirm:**
```
? Are you sure you want to log out of github.com account 'launchmaniac'? Yes
✓ Logged out of github.com account 'launchmaniac'
```

## Multiple Accounts

**Switch between accounts:**

```bash
gh auth login                    # Login to second account
gh auth switch                   # Switch between logged-in accounts
gh auth status                   # See all logged-in accounts
```

**Use specific account for command:**
```bash
gh repo list --hostname github.com --user account2
```

## OAuth Token vs Personal Access Token

**OAuth Token (gh auth login):**
- Created automatically via browser login
- Managed by GitHub CLI
- Stored securely in system keychain
- Refreshable
- **Use for:** Daily git operations, CLI commands

**Personal Access Token (for MCP):**
- Created manually in GitHub settings
- You manage expiration
- Stored in settings.json
- Specific scopes
- **Use for:** MCP integration, automation, scripts

**Both can coexist:**
- OAuth for CLI: `gh auth login`
- PAT for MCP: settings.json configuration

## Security Best Practices

**DO:**
- Use browser login (OAuth) for interactive use
- Regularly check `gh auth status`
- Logout on shared computers
- Use separate accounts for personal/work

**DON'T:**
- Share your authentication token
- Use same token across multiple computers
- Leave logged in on public computers

## Troubleshooting

**"authentication required" error:**
```bash
gh auth refresh
# or
gh auth login
```

**Git push still asks for password:**
```bash
gh auth login
# Select "Yes" when asked to authenticate Git
```

**Token expired:**
```bash
gh auth refresh
# Follow browser prompts
```

**Multiple accounts conflict:**
```bash
gh auth logout              # Logout all
gh auth login               # Login to primary account
```

## Token Location

**Where credentials are stored:**

- **Windows:** Windows Credential Manager
- **macOS:** Keychain
- **Linux:** `~/.config/gh/hosts.yml` (encrypted)

**To view (not recommended for security):**
```bash
gh auth status --show-token
```

## Automation

**For automation/CI/CD, use Personal Access Token:**

```bash
echo $GITHUB_TOKEN | gh auth login --with-token
```

Set `GITHUB_TOKEN` environment variable with PAT.

**Note:** For daily use, browser OAuth is more secure and convenient.
