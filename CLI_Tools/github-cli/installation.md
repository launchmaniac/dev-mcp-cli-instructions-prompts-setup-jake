# GitHub CLI (gh) Installation

## What is GitHub CLI?

Command-line tool for GitHub operations: push, pull, create repos, manage PRs/issues.

**Use for:**
- Authenticating git commands
- Creating/managing repositories
- Pull request workflows
- Issue management

**Different from GitHub MCP:**
- CLI = you/Claude run terminal commands
- MCP = Claude directly accesses GitHub API

## Installation

### Windows

**Option 1 - winget (recommended):**
```powershell
winget install GitHub.cli --accept-source-agreements --accept-package-agreements
```

**Option 2 - Manual download:**
- Download from: https://cli.github.com/
- Run installer
- Restart terminal

### Verification

**Close and reopen terminal**, then run:
```bash
gh --version
```

Should show: `gh version X.X.X`

## Authentication

**1. Run authentication:**
```bash
gh auth login
```

**2. Answer prompts:**
- **Account:** GitHub.com
- **Protocol:** HTTPS
- **Authenticate Git:** Yes
- **Method:** Login with a web browser

**3. Follow browser flow:**
- Copy 8-character code shown in terminal
- Press Enter (browser opens)
- Paste code → Authorize

**4. Verify:**
```bash
gh auth status
```

Should show: `✓ Logged in to github.com as [your-username]`

## Post-Installation Setup

**Configure git (if not already done):**
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

**Test authentication:**
```bash
gh repo list
```

Should show your repositories.

## Common Commands

**Repository operations:**
```bash
gh repo create my-new-repo --private
gh repo view launchmaniac/marketresearch-ai-assistant-jake
```

**Pull requests:**
```bash
gh pr create --title "Add feature X" --body "Description"
gh pr list
gh pr view 42
```

**Issues:**
```bash
gh issue create --title "Bug in X" --body "Details"
gh issue list
```

**Authentication:**
```bash
gh auth status          # Check login status
gh auth refresh         # Refresh credentials
gh auth logout          # Logout
```

## Troubleshooting

**"command not found: gh"**
- Restart terminal after installation
- Check PATH includes gh installation directory
- Reinstall using winget

**"Authentication required"**
- Run `gh auth login` again
- Check `gh auth status` for issues

**"Repository not found"**
- Check repository name spelling
- Verify you have access to the repo
- Try full path: `owner/repo`

## Integration with Git

After `gh auth login`, standard git commands authenticate automatically:

```bash
git push origin main          # No password needed
git clone https://github.com/user/repo.git
```

## Documentation

Official docs: https://cli.github.com/manual/
