# Architecture decisions before costly implementation

Design must explain *how* the approved behavior can be built, not invent new product obligations.

## Minimum design questions

- Boundaries/modules and why; interfaces between them; why not something simpler?
- Data model, ownership, tenant isolation (if applicable), migrations and retention.
- External APIs, authentication, consent, throttling, error/retry handling and cost.
- State transitions, concurrency, idempotency, audit, irreversible actions.
- Background work, outages, reconnection, recovery and graceful degradation.
- Environments, build/deployment, hosting, backup/restore, rollback and monitoring.
- Accessibility, responsive/device behavior and critical UX interaction states.
- Test seams, contract fixtures, observability and nonfunctional verification.

Use diagrams only when they reduce ambiguity. A component diagram, one data-flow diagram and a state table may be more useful than many pages of narrative.

## Architecture decision records (ADRs)

For each consequential decision, use [`templates/adr.md`](../templates/adr.md) with:

`Context → constraints → alternatives → decision → consequences → validation → status`

Prefer **simple, reversible choices** where tradeoffs are close. Document what would trigger revisiting a decision. Keep chosen products/versions explicitly project-dependent; this starter makes none.

## Design review checklist

- Does each critical requirement have a credible path to implementation and verification?
- Can an interruption, retry or concurrent actor corrupt state or duplicate business effects?
- Are secrets and authorization boundaries explicit, including admin/support access?
- Can migrations and schema changes roll back safely enough?
- Can files/artifacts and relational records be reconciled after partial failures?
- Are live-provider limits and cost exposure controlled?
- Is the selected local/CI environment representative of production where relevant?
- Which risks require actual device, cloud, integration or restore testing later?

If a design uncovers a product ambiguity, **return to requirement change control**; don't hide it inside a technical decision.
