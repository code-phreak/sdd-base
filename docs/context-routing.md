# Context routing — read the minimum necessary

**Always read:** `AGENTS.md` and the exact current prompt or user assignment. If a project exists, read only its `project/working-agreement.md` and the directly relevant current task/approved spec.

| Phase | Next documents (only if needed) |
|---|---|
| Intake | `docs/discovery.md`, `templates/project-brief.md` |
| Requirements | `docs/requirements.md`, `templates/requirements.md`, `templates/quality.md` |
| Architecture | `docs/architecture.md`, `templates/architecture.md`, `templates/adr.md` |
| Delivery planning | `docs/planning.md`, `templates/increment-*.md`, `templates/coverage.md` |
| Implementation | Current `project/increments/.../tasks.md`, relevant design and canonical requirement IDs; `docs/quality-verification.md` |
| Review / merge | `docs/git-collaboration.md`, `docs/approval-and-change-control.md` |
| Security / deployment | `docs/security-operations.md`, `docs/release-and-iteration.md` |
| Experience design | `docs/experience-design.md` |
| Change / new request | `docs/approval-and-change-control.md`, `docs/release-and-iteration.md` |

**Retrieval rules:**

1. Prefer file paths, headings, symbol search, and line ranges; don't dump whole directories or large files.
2. Read old conversations, execution logs, and historical decisions **only when a specific dependency or conflict requires them**.
3. Don't repeat canonical requirements in each feature document; cite IDs and read the definitions on demand.
4. Let tools/tests inspect large bodies of source and return bounded pass/fail summaries; preserve diagnostic logs outside Git when safe.
5. If context is missing, ask for the minimum missing decision. Never fabricate approvals or verification.

An agent may use existing project commands, but this template intentionally ships **no automation scripts or application code**. Generate appropriate tooling after the target stack and risks are understood.
