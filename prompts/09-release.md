# Prompt — readiness review and release planning

Follow `AGENTS.md`, `docs/release-and-iteration.md` and `docs/security-operations.md`. Review the approved release scope; **this prompt does not itself authorize production deployment**.

Prepare a concise go/no-go checklist with evidence for functional and quality requirements, full security/CI checks, manual UX/device tests, external integrations, migrations, backups/restore, rollback, monitoring, retention, costs, secrets and operational ownership. Explicitly separate **passed**, **pending**, **blocked**, and **exception requested**.

Use project-appropriate release versioning and artifact provenance only when approved. Propose a staged deployment/verification/rollback runbook. Ask for explicit approval before any production credentials, paid infrastructure, real-user migration, public availability, release tag, or deployment.

Once such authorization is actually granted in a separate turn, execute **only** the approved deployment window and verify its results. Never silently convert release readiness review into deployment.
