# Codebase Definition Template

**Purpose:** This template provides a structured framework for comprehensively defining any codebase. Use this to create a complete technical reference that helps both humans and AI understand the project architecture, patterns, and implementation details.

**When to Use:** Beginning of new projects, documenting existing codebases, onboarding developers, or providing deep context to AI assistants.

**Update Frequency:** Quarterly or at major milestones

---

## Instructions for AI

When asked to create a codebase definition, use this template to structure the documentation. Fill in all applicable sections with specific details about the project. Skip sections that are not relevant, but explain why they don't apply.

Focus on:
- Accuracy and specificity over generalization
- Concrete examples rather than abstract descriptions
- Practical information that helps someone understand and work with the code
- Technical depth appropriate for developers who will work on the project

---

## 1. Project Identity

### Project Name
[Official project name]

### Project Type
- [ ] Web Application
- [ ] Mobile Application
- [ ] API/Backend Service
- [ ] CLI Tool
- [ ] Library/Package
- [ ] Desktop Application
- [ ] Full-Stack Application
- [ ] Microservice
- [ ] Other: ___________

### One-Line Description
[Concise description of what this project does]

### Core Purpose
[2-3 paragraphs explaining why this project exists, what problem it solves, and who it serves]

### Version
Current Version: [e.g., v1.2.3]
Release Date: [Date]

---

## 2. Technical Foundation

### Primary Language(s)
- **Language:** [e.g., TypeScript]
- **Version:** [e.g., 5.3.x]
- **Percentage of Codebase:** [e.g., 85%]

[Repeat for additional languages]

### Runtime Environment
- **Environment:** [e.g., Node.js, Browser, Python, etc.]
- **Version:** [e.g., 20.x]
- **Target Platforms:** [e.g., Linux, macOS, Windows, iOS, Android]

### Framework(s)
- **Primary Framework:** [e.g., React, Vue, Express, FastAPI]
- **Version:** [e.g., 18.x]
- **Purpose:** [Why this framework was chosen]

### Key Dependencies
List the 5-10 most critical dependencies:

| Dependency | Version | Purpose | Critical? |
|------------|---------|---------|-----------|
| [name] | [version] | [what it does] | Yes/No |

---

## 3. Architecture Overview

### Architectural Pattern
- [ ] Monolithic
- [ ] Microservices
- [ ] Serverless
- [ ] JAMstack
- [ ] Modular Monolith
- [ ] Event-Driven
- [ ] Layered Architecture
- [ ] Other: ___________

### High-Level Architecture Diagram
```
[ASCII diagram or description of major system components and their relationships]

Example:
┌─────────────┐
│   Client    │
└──────┬──────┘
       │
       ↓
┌─────────────┐
│   API Layer │
└──────┬──────┘
       │
       ↓
┌─────────────┐
│  Database   │
└─────────────┘
```

### Data Flow
Describe how data moves through the system:
1. [Entry point]
2. [Processing steps]
3. [Storage/output]

### State Management
- **Approach:** [e.g., Redux, Vuex, Context API, Server-side sessions]
- **Scope:** [Where state lives: client, server, both]

---

## 4. Directory Structure

### Root Structure
```
project-root/
├── src/              # [Description]
├── tests/            # [Description]
├── docs/             # [Description]
├── config/           # [Description]
├── scripts/          # [Description]
├── public/           # [Description]
└── dist/             # [Description]
```

### Key Directory Purposes

**`/src/`**
- Purpose: [Main application source code]
- Key subdirectories:
  - `/src/components/` - [Description]
  - `/src/services/` - [Description]
  - `/src/utils/` - [Description]

**`/tests/`**
- Purpose: [Test files and test utilities]
- Organization: [e.g., mirrors src/ structure, organized by type]

**`/config/`**
- Purpose: [Configuration files for different environments]
- Key files:
  - `config.dev.json` - [Development settings]
  - `config.prod.json` - [Production settings]

[Add all relevant directories]

### File Naming Conventions
- Components: [e.g., PascalCase.tsx]
- Utilities: [e.g., camelCase.ts]
- Tests: [e.g., fileName.test.ts]
- Styles: [e.g., fileName.module.css]
- Constants: [e.g., UPPER_SNAKE_CASE.ts]

---

## 5. Core Modules & Components

### Module Map
List major functional modules/domains:

1. **[Module Name]** (`/src/path/to/module/`)
   - **Purpose:** [What this module does]
   - **Key Files:**
     - `file1.ts` - [Description]
     - `file2.ts` - [Description]
   - **Dependencies:** [Other modules this depends on]
   - **Exports:** [What this module provides to others]

2. **[Module Name]**
   [Repeat structure]

### Entry Points
- **Main Entry:** [e.g., `/src/index.ts` - Application bootstrap]
- **Secondary Entries:** [e.g., `/src/worker.ts` - Background job processor]

### Critical Components/Classes
List the 5-10 most important components:

**[ComponentName]** (`/src/path/to/Component.tsx`)
- **Purpose:** [What it does]
- **Props/Parameters:** [Key inputs]
- **Usage:** [Where/how it's used]
- **Dependencies:** [What it relies on]

---

## 6. Configuration Management

### Environment Variables
List all environment variables:

| Variable Name | Required? | Default | Purpose | Example |
|---------------|-----------|---------|---------|---------|
| `DATABASE_URL` | Yes | None | Database connection string | `postgresql://...` |
| `API_KEY` | Yes | None | External API authentication | `sk_test_...` |
| `PORT` | No | `3000` | Server port | `8080` |

### Configuration Files
- **Location:** [e.g., `/config/` or root]
- **Format:** [e.g., JSON, YAML, .env]
- **Environment-Specific:** [How configs differ per environment]

### Feature Flags
If applicable:
- **System:** [e.g., LaunchDarkly, custom, environment variables]
- **Key Flags:**
  - `FEATURE_NEW_UI` - [Description]
  - `ENABLE_BETA` - [Description]

---

## 7. Data Layer

### Database(s)
**Primary Database:**
- **Type:** [e.g., PostgreSQL, MongoDB, MySQL]
- **Version:** [e.g., 15.x]
- **ORM/Query Builder:** [e.g., Prisma, TypeORM, Mongoose]
- **Schema Location:** [e.g., `/prisma/schema.prisma`]
- **Migrations:** [Where/how managed]

**Secondary Database(s):**
[If applicable, repeat structure]

### Data Models
List core entities:

**[EntityName]**
```typescript
// Example structure
interface User {
  id: string
  email: string
  createdAt: Date
  // ... key fields
}
```
- **Table/Collection:** [Name in database]
- **Relationships:** [Related entities]

### Caching
- **System:** [e.g., Redis, in-memory, CDN]
- **What's Cached:** [Types of data]
- **TTL Strategy:** [Cache expiration approach]

---

## 8. External Integrations

### APIs & Services
List all external services:

| Service | Purpose | Authentication | Documentation |
|---------|---------|----------------|---------------|
| [Service Name] | [What it's used for] | [API key, OAuth, etc.] | [Link] |

### Webhooks
**Incoming Webhooks:**
- Endpoint: [URL pattern]
- Source: [Service name]
- Purpose: [What triggers it]

**Outgoing Webhooks:**
- Triggers: [What causes them]
- Destinations: [Where they go]

---

## 9. Authentication & Authorization

### Authentication Method
- [ ] JWT
- [ ] Session-based
- [ ] OAuth 2.0
- [ ] API Keys
- [ ] Other: ___________

### User Roles
| Role | Permissions | Access Level |
|------|-------------|--------------|
| Admin | [Description] | Full access |
| User | [Description] | Limited |

### Security Considerations
- Password hashing: [e.g., bcrypt, Argon2]
- Token storage: [Where/how]
- CORS policy: [Configuration]
- Rate limiting: [Implementation]

---

## 10. Build & Development

### Package Manager
- **Tool:** [e.g., npm, yarn, pnpm, pip]
- **Version:** [e.g., pnpm 8.x]
- **Lock File:** [e.g., pnpm-lock.yaml]

### Build Process
**Development Build:**
```bash
# Command to run dev server
npm run dev
```
- Hot reload: [Yes/No]
- Source maps: [Yes/No]

**Production Build:**
```bash
# Command to build for production
npm run build
```
- Output location: [e.g., `/dist/`]
- Minification: [Yes/No]
- Tree shaking: [Yes/No]

### Scripts
List key package.json scripts:

| Script | Command | Purpose |
|--------|---------|---------|
| `dev` | `vite dev` | Start development server |
| `build` | `vite build` | Production build |
| `test` | `vitest` | Run test suite |
| `lint` | `eslint .` | Code linting |
| `type-check` | `tsc --noEmit` | TypeScript validation |

---

## 11. Testing Strategy

### Testing Framework(s)
- **Unit Tests:** [e.g., Jest, Vitest]
- **Integration Tests:** [Framework]
- **E2E Tests:** [e.g., Playwright, Cypress]

### Test Organization
- Location: [e.g., `/tests/` or co-located with source]
- Naming: [e.g., `*.test.ts`, `*.spec.ts`]
- Coverage Target: [e.g., 80%]

### Running Tests
```bash
# Unit tests
npm run test

# E2E tests
npm run test:e2e

# Coverage report
npm run test:coverage
```

### Mocking Strategy
- API mocks: [How handled]
- Database mocks: [Approach]
- External service mocks: [Method]

---

## 12. Code Quality & Standards

### Linting
- **Tool:** [e.g., ESLint]
- **Config:** [e.g., `.eslintrc.js`]
- **Rules:** [Standard, Airbnb, custom]

### Formatting
- **Tool:** [e.g., Prettier]
- **Config:** [e.g., `.prettierrc`]
- **Integration:** [Pre-commit hook, CI]

### Type Checking
- **System:** [e.g., TypeScript, Flow, JSDoc]
- **Strictness:** [strict mode enabled?]
- **Check Command:** [e.g., `npm run type-check`]

### Git Hooks
- **Tool:** [e.g., Husky, pre-commit]
- **Pre-commit:** [What runs before commit]
- **Pre-push:** [What runs before push]

### Commit Conventions
- **Style:** [e.g., Conventional Commits]
- **Format:** `type(scope): description`
- **Types:** feat, fix, docs, chore, refactor, test, style

---

## 13. Deployment & DevOps

### Hosting Platform
- **Platform:** [e.g., Render, Vercel, AWS, Hetzner]
- **Region:** [e.g., US East, EU West]
- **URL:** [Production URL]

### Deployment Process
**Trigger:** [e.g., Push to main branch, Manual deploy, Tag creation]

**Pipeline Steps:**
1. [e.g., Checkout code]
2. [e.g., Install dependencies]
3. [e.g., Run tests]
4. [e.g., Build application]
5. [e.g., Deploy to platform]

### Environments
| Environment | URL | Branch | Purpose |
|-------------|-----|--------|---------|
| Development | [URL] | `develop` | Active development |
| Staging | [URL] | `staging` | Pre-production testing |
| Production | [URL] | `main` | Live application |

### CI/CD
- **Platform:** [e.g., GitHub Actions, GitLab CI, CircleCI]
- **Config Location:** [e.g., `.github/workflows/`]
- **Key Workflows:**
  - `deploy.yml` - [Description]
  - `test.yml` - [Description]

### Environment Variables Management
- **Tool:** [e.g., Platform dashboard, Doppler, AWS Secrets Manager]
- **Access:** [Who can modify]

---

## 14. Monitoring & Observability

### Logging
- **System:** [e.g., Winston, Pino, console]
- **Levels:** [debug, info, warn, error]
- **Storage:** [Where logs go]

### Error Tracking
- **Service:** [e.g., Sentry, Rollbar, custom]
- **Integration:** [How implemented]

### Performance Monitoring
- **Tool:** [e.g., New Relic, DataDog, custom]
- **Metrics Tracked:**
  - [e.g., Response time]
  - [e.g., Memory usage]
  - [e.g., Request rate]

### Uptime Monitoring
- **Service:** [e.g., UptimeRobot, Pingdom]
- **Endpoints Monitored:** [List critical endpoints]

---

## 15. Documentation

### Code Documentation
- **Style:** [e.g., JSDoc, TSDoc, docstrings]
- **Coverage:** [What's documented]
- **Generation:** [e.g., TypeDoc, JSDoc]

### API Documentation
- **Format:** [e.g., OpenAPI/Swagger, Postman]
- **Location:** [URL or file path]
- **Auto-generated:** [Yes/No]

### Project Documentation
- **README.md** - [Quick start and overview]
- **CONTRIBUTING.md** - [How to contribute]
- **CHANGELOG.md** - [Version history]
- **API.md** - [API reference]
- **/docs/** - [Detailed documentation]

### Runbooks
Location of operational guides:
- Deployment procedure: [Link/location]
- Incident response: [Link/location]
- Database migrations: [Link/location]

---

## 16. Development Workflow

### Getting Started
**Prerequisites:**
- [e.g., Node.js 20+]
- [e.g., PostgreSQL 15+]
- [e.g., pnpm 8+]

**Setup Steps:**
```bash
# 1. Clone repository
git clone [repo-url]
cd [project-name]

# 2. Install dependencies
pnpm install

# 3. Set up environment
cp .env.example .env
# Edit .env with your values

# 4. Set up database
pnpm run db:setup

# 5. Start development server
pnpm run dev
```

### Daily Development Commands
```bash
# Start dev server
pnpm run dev

# Run tests in watch mode
pnpm run test:watch

# Type check
pnpm run type-check

# Lint and fix
pnpm run lint:fix
```

### Branch Strategy
- **Model:** [e.g., Git Flow, GitHub Flow, Trunk-based]
- **Main Branch:** [e.g., `main`]
- **Development Branch:** [e.g., `develop`]
- **Feature Branches:** [e.g., `feat/feature-name`]
- **Hotfix Branches:** [e.g., `hotfix/issue-description`]

### Pull Request Process
1. [Create feature branch from develop]
2. [Make changes and commit]
3. [Push branch and open PR]
4. [Request review from team]
5. [Address feedback]
6. [Merge after approval]

---

## 17. Common Tasks & Recipes

### Add a New Feature
1. [Create feature branch]
2. [Create component/module]
3. [Write tests]
4. [Update documentation]
5. [Submit PR]

### Database Migrations
```bash
# Create migration
pnpm run db:migrate:create [name]

# Run migrations
pnpm run db:migrate

# Rollback migration
pnpm run db:migrate:rollback
```

### Adding Dependencies
```bash
# Production dependency
pnpm add [package-name]

# Development dependency
pnpm add -D [package-name]

# Update all dependencies
pnpm update
```

### Debugging
**Development:**
- [e.g., Browser DevTools, VS Code debugger]
- Breakpoints: [How to set]
- Logging: [Where to add]

**Production:**
- [Error tracking service]
- [Log aggregation]
- [Performance profiling]

---

## 18. Known Issues & Limitations

### Current Limitations
1. [Limitation 1 - Description and workaround]
2. [Limitation 2 - Description and workaround]

### Known Bugs
| Issue | Severity | Status | Workaround |
|-------|----------|--------|------------|
| [Description] | High/Med/Low | Open/In Progress | [Workaround] |

### Technical Debt
1. [Technical debt item 1]
   - Impact: [Description]
   - Plan: [How/when to address]

---

## 19. Performance Considerations

### Bundle Size
- **Target:** [e.g., < 200KB gzipped]
- **Current:** [Size]
- **Optimization Strategies:**
  - [e.g., Code splitting]
  - [e.g., Lazy loading]
  - [e.g., Tree shaking]

### Load Time
- **Target:** [e.g., < 3s Time to Interactive]
- **Current:** [Metric]

### Scalability
- **Current Capacity:** [e.g., 1000 concurrent users]
- **Bottlenecks:** [Known limitations]
- **Scaling Strategy:** [Horizontal/Vertical, when to scale]

---

## 20. Security Checklist

- [ ] Environment variables secured (not in code)
- [ ] Secrets encrypted at rest
- [ ] HTTPS enforced in production
- [ ] Input validation on all endpoints
- [ ] SQL injection protection
- [ ] XSS prevention
- [ ] CSRF protection
- [ ] Rate limiting implemented
- [ ] Authentication required for protected routes
- [ ] Authorization checks in place
- [ ] Dependencies regularly updated
- [ ] Security headers configured
- [ ] Sensitive data encrypted in database
- [ ] Audit logging for sensitive operations

---

## 21. Team & Contacts

### Project Ownership
- **Product Owner:** [Name/Email]
- **Tech Lead:** [Name/Email]
- **Primary Maintainer:** [Name/Email]

### Key Contributors
| Name | Role | Focus Area | Contact |
|------|------|------------|---------|
| [Name] | [Role] | [Area] | [Email/Slack] |

### Communication Channels
- **Chat:** [e.g., Slack #project-name]
- **Issues:** [e.g., GitHub Issues]
- **Documentation:** [e.g., Notion, Confluence]
- **Meetings:** [Cadence and purpose]

### Project Management Integration

**ClickUp Integration:**
- **Workspace:** [ClickUp workspace name and URL]
- **Space:** [Project space name and URL]
- **Key Lists:**
  - Backlog: [List URL]
  - Current Sprint: [List URL]
  - Epics: [List URL]

**Integration Method:** ClickUp MCP via markdown templates
- **Workspace Template:** `project-workspace.md`
- **Sync Guide:** `clickup-sync-guide.md`
- **Configuration:** `clickup-mapping-config.yaml`
- **Sync Workflow:** Templates → ClickUp (work in markdown, sync for team visibility)

---

## 22. Reference Links

### External Documentation
- [Service/Tool Name]: [Documentation URL]

### Related Projects
- [Related Project]: [Repository URL]

### Learning Resources
- [Resource Name]: [URL]

---

## 23. Change Log

### Version History
**[Version] - [Date]**
- Added: [New features]
- Changed: [Modifications]
- Fixed: [Bug fixes]
- Removed: [Deprecated features]

---

## 24. Appendices

### A. Glossary
- **[Term]:** [Definition]

### B. Architecture Decision Records (ADRs)
Location: [e.g., `/docs/adr/`]

List of key decisions:
1. [ADR-001: Decision Title] - [Date]

### C. Dependency Graph
[Visual or text representation of module dependencies]

### D. API Endpoints Reference
[Quick reference table if not using OpenAPI]

| Method | Endpoint | Purpose | Auth Required |
|--------|----------|---------|---------------|
| GET | `/api/users` | List users | Yes |

---

**Document Maintenance:**
- Last Updated: [Date]
- Updated By: [Name]
- Next Review: [Date]

---

**Product of Launch Maniac LLC, Las Vegas, Nevada**
**(725) 444-8200 | support@launchmaniac.com**
