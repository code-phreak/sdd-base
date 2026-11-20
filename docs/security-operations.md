# Security, privacy and operations by design

Pick controls proportionate to your data, deployment and threat model. The framework ships no credentials or infrastructure.

## Before any integration

- Identify actors, permissions, tenant boundaries, support/admin access and audit requirements.
- Separate application login from third-party authorization; use least necessary scopes, user-facing consent, token rotation and revocation.
- Decide which input data may be sent to external APIs and under what disclosure/consent. Do not use real sensitive data in public fixtures or logs.
- Validate cost/rate limits, timeouts, retries and credential-handling requirements. Paid API access needs explicit approval.
- Model idempotency, optimistic concurrency, evidence history, and partial failures for workflows with consequential effects.

## Before publishing code

- Keep secrets in ignored local files or approved secret stores, never in the frontend bundle, fixtures, prompts, CI output, PRs or Git history.
- Scan candidate files and relevant history. If leaked, revoke/rotate and clean history through an explicitly approved process—not a silent force-push.
- Use dependency and license checks appropriate to the stack and release audience.
- Use synthetic fixtures unless legitimate real-data testing has been explicitly authorized and isolated.

## Before deploying

- Separate development/test from production secrets and data; review environment variable handling and allowed outbound requests.
- Use reviewed migrations, backup verification, rollback/forward-recovery planning, health checks and observability. App startup should not make risky schema changes without a deliberate procedure.
- Validate storage and database restore **together**, including object/file checksums and orphaned operations where applicable.
- Set retention rules for data vs short-lived backups vs diagnostic logs; they serve different purposes.
- Define monitoring, ownership of alerts, incident response, user deletion requests, provider outages and cost ceilings.
- Test in the actual production-relevant environment and record remaining live acceptance. A local mock is not proof of hosted or external API behavior.

## Threat review

For small projects, answer: *What data matters? Who might access it? What could be lost, corrupted, misdirected or abused? What control detects or limits the event? How do we recover?* For higher-risk systems, use [`templates/threat-model.md`](../templates/threat-model.md) and review after architectural changes.

Security is a **continuous implementation constraint**, not a final increment where all protections are added.
