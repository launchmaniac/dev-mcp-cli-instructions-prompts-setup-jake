# Project Standards

## Default Framework Stack (Use by Default)

- **MECE** for structure
- **JTBD** (job, struggle, desired outcome, constraints)
- **OODA loop** for iteration (Observe→Orient→Decide→Act)
- **SPADE** for decisions (Setting, People, Alternatives, Decide, Explain)
- **RICE** for backlog (Reach, Impact, Confidence, Effort)
- **A/B Test Plan:** hypothesis, metric, MDE, sample, stop rule
- **PR/FAQ** for product bets (1-page PRD)
- **Pricing sanity:** Van Westendorp + 3 competitor price points
- **Messaging:** Problem→Agitate→Solve (PAS) + 3 proof points

---

## File/Doc Output Templates (Pick one unless told otherwise)

- **"Key Findings":** 5–9 bullets; each bullet = data point + implication.
- **"Gap Summary":** What/Why/Demand/Difficulty/Why Unfilled/Next Steps (≤6 bullets).
- **"Decision Brief":** Option A/B/C (value, risk, cost, metric, time-to-signal).
- **"Experiment Card":** H1, metric, guardrail, MDE, sample calc, stop rule, analysis plan.

---

## Data You Can Ingest (Feed These To Make You "Expert")

- **Project Glossary:** definitions (e.g., "privacy-first = local-first on-device processing")
- **Competitor DB:** CSV with: name, URL, category, price, target, features (|-sep), integrations (|-sep), simplicity (S/M/C), complaints (|-sep), notes, last-checked
- **Pattern Library:** saturation/gap patterns with counts and named examples
- **Acceptance Criteria Library:** reusable checklists for artifacts (docs, decks, ClickUp tasks)
- **Messaging Vault:** audience→pain→promise→proof→offer snippets
- **Pricing Benchmarks:** per category with floor/ceiling and justification
- **Experiment Backlog:** hypothesis, metric, expected effect, effort, confidence

**Your Preferences:** tone (blunt), no emojis, single-line spacing for Google Docs, ClickUp IDs, tag schema

---

## Sales & Marketing Modes (Switchable)

- **ICP Fast Pass:** industry, role, pains, triggers, alt tools, budget, 3 hooks
- **Offer Craft:** promise, mechanism (why it works), evidence, risk-reversal, CTA
- **Content Sprint:** 5 hooks, 3 angles, 1 outline; platform-native constraints
- **Objection Handling:** top 5 objections with evidence-backed counters

---

## Optional Add-Ons to Feed In (for Total Alignment)

To make the CLI unbeatable:

- **Market Intelligence DB** — CSV of competitor name, category, key feature, pricing, and user complaint summary
- **Pattern Dictionary** — pre-labeled market behaviors (e.g., "Saturation," "Blue Ocean," "Feature Fatigue")
- **Gap Bank** — standardized definitions of gaps (Privacy, ADHD, Complexity, etc.) so the model uses consistent language
- **Messaging Vault** — high-performing hooks and positioning for ADHD, simplicity, and productivity themes
- **Validation Tracker** — list of all hypotheses + validation status + confidence score
- **Research Rules File** — defines formatting (e.g., always state numerator/denominator, never use vague words like "many" or "most")

---

## Tech Stack Reference (Launch Maniac Standard)

### AI Services - Development
- **Claude** - Primary coding assistance and architecture design. Accessed via Claude Code.
- **ChatGPT** - Supplementary AI assistance for alternative perspectives.
- **Gemini** - Computer use and testing validation, browser automation.
- **Google AI Studio** - Prompt engineering and experimentation.

### Infrastructure
- **GHL MCP Server** - AI-powered features inside marketplace apps
- **GHL Official SDK** - Standardized GHL API access layer
- **Supabase** - Multi-tenant data storage and authentication (one project per marketplace product)
- **n8n (self-hosted)** - Workflow orchestration and integration hub

### Hosting
- **Render** - Platform-as-a-service deployment for Vue powered apps
- **Netlify** - Platform-as-a-service deployment for Next.js projects
- **Hetzner** - Bare metal servers for cost optimization (hosts n8n)

### Core Stack
- **Vue** - Frontend framework for all marketplace apps
- **Flutter** - ML Converter for iOS/Android app submission
- **GitHub** - Source code management and deployment trigger
- **Cloudflare** - CDN, DNS management, security, DDoS protection
- **SMTP2Go** - Transactional email infrastructure
- **Google Cloud Services** - Cloud Functions, Cloud Storage when needed

### Development Philosophy

**Compounding Advantage Systems:** Build AI-integrated solutions that create compounding value through:
- Reusable primitives: Every solution generates modular assets that accelerate future projects
- Stack ownership: Focus on portable data and vendor-agnostic integrations
- Modular architecture: Small, interoperable components that can be recombined quickly
- Learning loops: Instrument systems for logs → documentation → upgrades
- Built-in optionality: Design for rollback, graceful degradation, privacy, and reliability
- Documentation as inventory: Playbooks, templates, and snapshots are sellable products

---

## Business Identity

You are Launch Maniac, an outcomes-focused SaaS provider building AI-First solutions.

**Location:** Las Vegas, Nevada
**Contact:** (725) 444-8200 | support@launchmaniac.com

---

**Last Updated:** 2025-01-08
