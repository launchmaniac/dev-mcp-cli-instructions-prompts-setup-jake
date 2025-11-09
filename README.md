# Launch Maniac MCP & CLI Setup

**Single source of truth for all MCP servers, CLI tools, and prompt configurations.**

## Quick Start

1. Clone this repository on any new computer
2. Follow installation guides in respective folders
3. Copy CLAUDE.md to `~/.claude/CLAUDE.md`
4. Configure MCP servers using settings.json

## Repository Structure

```
launchmaniac-mcp-cli-setup/
├── README.md (this file)
├── CLAUDE.md (operator profile for Claude Code)
│
├── MCP_Servers/
│   ├── clickup/ - ClickUp MCP integration
│   └── github/ - GitHub MCP integration
│
├── CLI_Tools/
│   └── github-cli/ - GitHub CLI (gh) setup
│
├── Prompt_Templates/
│   ├── EPIC_Framework.md
│   ├── Research_Contracts.md
│   ├── Decision_Briefs.md
│   └── Gap_Analysis.md
│
└── Claude_Code_Settings/
    └── settings.json (MCP configurations)
```

## Installation Order

1. **GitHub CLI** - Required for authentication
2. **ClickUp MCP** - Task management integration
3. **GitHub MCP** - Repository management integration
4. **CLAUDE.md** - Copy to `~/.claude/` for operator profile

## Usage

- Each MCP/CLI folder contains installation and authentication guides
- Prompt templates are reusable across all projects
- Settings.json contains working MCP configurations

## Support

Repository: https://github.com/launchmaniac/launchmaniac-mcp-cli-setup
Contact: support@launchmaniac.com
