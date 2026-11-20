# Reusable agent prompts

Copy the relevant prompt into **your agent's chat**. The files are instructions, not scripts. Most agents can read the repository and follow them directly; no special integration is required.

| Stage | Prompt |
|---|---|
| Begin with an idea or existing code | [`00-start.md`](00-start.md) |
| Deepen discovery (optional) | [`01-discover.md`](01-discover.md) |
| Define verifiable requirements | [`02-requirements.md`](02-requirements.md) |
| Make architectural decisions | [`03-architecture.md`](03-architecture.md) |
| Map increments and tasks | [`04-plan.md`](04-plan.md) |
| Scaffold and establish toolchain | [`05-bootstrap.md`](05-bootstrap.md) |
| Authorize just one task | [`06-task.md`](06-task.md) |
| Authorize a complete increment | [`07-increment.md`](07-increment.md) |
| Review and merge | [`08-review.md`](08-review.md) |
| Prepare deployment/release | [`09-release.md`](09-release.md) |
| Triage feedback / change a spec | [`10-iterate.md`](10-iterate.md) |
| Start a fresh agent conversation | [`11-handoff.md`](11-handoff.md) |
| Facilitate a UI/UX review | [`12-experience.md`](12-experience.md) |
| Audit cross-feature completeness | [`13-audit.md`](13-audit.md) |

**Recommended flow:** `00 → 02 → 03 → 04 → 13 → 05 → 06 or 07 → 08 → 09 → 10`. Add `01` when discovery needs more depth, `11` between conversations, and `12` for significant user-facing experience decisions. Small projects may combine stages.

Replace bracketed placeholders with your intent. If you omit them, the agent should use the current project's explicit approved state, not guess. For irreversible changes, confirm the developer's authorization rather than interpreting this template as permission.

**Efficiency:** One conversation per increment is a useful default, but avoid reloading prior chats. The current approved specs and source code are the working context.
