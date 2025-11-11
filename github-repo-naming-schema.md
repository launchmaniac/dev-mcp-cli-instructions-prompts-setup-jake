# GitHub Repository Naming Schema

## Official Format

```
[department]-[category]-[project-name]-[initials]
```

**Example:** `marketing-marketresearch-competitor-analysis-jw`

---

## Department List

Use these exact department names (case-sensitive):

- `ops` - Operations
- `dev` - Development
- `admin` - Administration
- `marketing` - Marketing
- `sales` - Sales
- `training` - Training

---

## Category List

Use these exact category names (case-sensitive):

- `marketresearch` - Market Research
- `report` - Reports and Analysis
- `workflow` - Workflow Automation
- `snapshot` - Snapshots and Status Updates
- `tool` - Tools and Utilities
- `documentation` - Documentation Projects
- `automation` - Automation Scripts
- `dashboard` - Dashboards and Visualizations
- `integration` - System Integrations
- `project` - General Projects

---

## Naming Rules

### 1. **Format Requirements**
- All lowercase
- Use hyphens (`-`) as separators between sections
- No spaces, underscores, or special characters
- Format: `[department]-[category]-[project-name]-[initials]`

### 2. **Department Section**
- Single word from the approved department list
- No hyphens within the department name

### 3. **Category Section**
- Single word/compound word from the approved category list
- No hyphens within the category name (e.g., `marketresearch` not `market-research`)

### 4. **Project Name Section**
- Descriptive name for the project
- Use hyphens to separate words (e.g., `competitor-analysis`, `ai-assistant`)
- Keep it concise but meaningful (2-4 words recommended)
- Use descriptive terms that explain what the project does

### 5. **Initials Section**
- Two-letter lowercase initials (e.g., `jw` for Jake Whitbeck)
- Always at the end
- Helps identify project owner at a glance

---

## Examples by Department

### Operations (ops)
- `ops-workflow-inventory-management-jw`
- `ops-report-monthly-metrics-jw`
- `ops-automation-data-sync-jw`

### Development (dev)
- `dev-tool-api-wrapper-jw`
- `dev-integration-payment-gateway-jw`
- `dev-project-mobile-app-jw`

### Administration (admin)
- `admin-documentation-employee-handbook-jw`
- `admin-workflow-onboarding-automation-jw`
- `admin-report-quarterly-review-jw`

### Marketing (marketing)
- `marketing-marketresearch-competitor-analysis-jw`
- `marketing-marketresearch-ai-assistant-jw`
- `marketing-report-campaign-results-jw`
- `marketing-automation-email-sequences-jw`

### Sales (sales)
- `sales-dashboard-pipeline-tracker-jw`
- `sales-report-quarterly-performance-jw`
- `sales-tool-lead-scorer-jw`

### Training (training)
- `training-documentation-product-guide-jw`
- `training-workflow-onboarding-checklist-jw`
- `training-snapshot-weekly-progress-jw`

---

## Do's and Don'ts

### ✅ DO
- Use all lowercase
- Use approved department and category names
- Keep project names descriptive and concise
- Use hyphens to separate words in project name
- Always include initials at the end
- Be consistent with naming patterns

### ❌ DON'T
- Use spaces or underscores
- Use capital letters
- Add hyphens within department or category names
- Use abbreviations that aren't clear
- Make project names too long (avoid 5+ words)
- Include version numbers in repo name (use tags/releases instead)
- Use special characters (@, #, $, etc.)

---

## Valid Examples

✅ `marketing-marketresearch-ai-assistant-jw`
✅ `dev-automation-workflow-builder-jw`
✅ `ops-report-quarterly-analysis-jw`
✅ `sales-dashboard-pipeline-metrics-jw`
✅ `training-documentation-product-onboarding-jw`

## Invalid Examples

❌ `Marketing-MarketResearch-AI-Assistant-JW` (capitals)
❌ `marketing_marketresearch_ai_assistant_jw` (underscores)
❌ `marketing-market-research-ai-assistant-jw` (hyphen in category)
❌ `marketresearch-ai-assistant-jw` (missing department)
❌ `marketing-ai-assistant-jw` (missing category)
❌ `marketing-marketresearch-ai-assistant` (missing initials)

---

## GitHub Organization Tips

1. **Searchability:** Repos are searchable by any part of the name
   - Search `marketing-` to find all marketing repos
   - Search `marketresearch-` to find all market research repos
   - Search `-jw` to find all Jake's repos

2. **Sorting:** GitHub sorts repos by last change by default
   - Most recently updated repos appear first
   - Use naming consistency for easier filtering

3. **Topics/Tags:** Use GitHub topics to add additional metadata
   - Add tags like: `ai`, `automation`, `analysis`, `active`, `archived`
   - Topics supplement the naming schema for better organization

4. **Description:** Always add a clear one-line description
   - Explains what the repo does
   - Appears in search results

---

## Team Member Initials

| Name | Initials |
|------|----------|
| Jake Whitbeck | jw |
| [Add team members here] | [initials] |

---

## Adding New Categories

If you need a new category:
1. Discuss with team to ensure it's distinct from existing categories
2. Use a single compound word (no hyphens)
3. Add it to the official category list above
4. Document examples of its usage

---

## Version History

- **v1.0** - Initial naming schema created (2025-11-11)
  - Format: `[department]-[category]-[project-name]-[initials]`
  - 6 departments, 10 categories defined
  - Established for Jake Whitbeck (jw)
