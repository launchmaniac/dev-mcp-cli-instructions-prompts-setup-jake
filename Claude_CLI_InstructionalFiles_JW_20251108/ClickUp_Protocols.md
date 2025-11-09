# ClickUp Protocols

## ClickUp EPIC Framework (Strict)

**EPIC = process outcome, not product success.**

Parent task ≠ label: it has synthesis work.

### Structure per EPIC:

**Parent Task (SYNTHESIS):**
- Write plan (start)
- Monitor alignment (during)
- Integrate deliverables (end)
- "Done" = integrated doc + pass/fail vs criteria

**Subtasks (WORK):**
- 3–7 atomic outputs
- Each with clear artifact and acceptance criteria

### Cross-EPIC Dependencies:

- EPIC 1 outputs = criteria for EPIC 2
- EPIC 2 outputs = evidence for EPIC 3

### Acceptance Criteria Template (use everywhere):

- Artifact link
- Measurable quality bar
- Reviewer
- Deadline
- Blocker rules

---

## Active-Task Discipline (No Jumping)

Track and show state in every reply:

- **Current Phase:** EPIC #: Subtask #
- **You Are Here:** 1-sentence objective
- **Next Atomic Step:** verb + artifact + timebox
- **Exit Criteria:** bullet list

If asked to switch, warn of impact and offer a parked note.

---

## ClickUp Time Tracking (MANDATORY)

### When STARTING a task:
- Confirm task ID with user before starting timer
- Start time tracking: `mcp__clickup__clickup_start_time_tracking` with task_id
- Acknowledge: "Timer started on [task_id]: [task_name]"

### When COMPLETING a task:
- Stop time tracking: `mcp__clickup__clickup_stop_time_tracking`
- Update task status to complete
- Acknowledge: "Timer stopped, task marked complete"

### If switching tasks mid-work:
- Stop current timer first
- Start new timer on new task
- Warn user about context switch cost

---

## ClickUp Task Creation (MANDATORY fields)

When creating tasks, ALWAYS include:

- **assignees:** `["jake@launchmaniac.com"]` (NEVER omit)
- **priority:** `"high"` | `"urgent"` | `"normal"` | `"low"` (NEVER omit)
- **due_date:** `"YYYY-MM-DD"` format (NEVER omit)
- **start_date:** `"YYYY-MM-DD"` format (recommended)
- **tags:** `["epic-X", "research", etc.]` (NEVER omit)
- **markdown_description:** Full context with objective, dependencies, deliverables, exit criteria

---

## EPIC Completion Requirements

Every EPIC must have final subtask:
- Update Activity Log
- Update Journal Doc (Google Doc with findings)
- Team Review (EPIC 3 only)
- Mark EPIC complete

---

## Activity Log Protocol

### When task completes + timer stops:
- Auto-write entry to Activity Log (silent, no interrupt)

### Entry format:
- Date/time
- Task name
- Duration
- Key output (1-2 sentences)
- Blockers
- Next

### At EPIC end:
- Review all entries for accuracy
- Update if needed

---

**Last Updated:** 2025-01-08
