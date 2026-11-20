# Who approves what, and how changes remain safe

## Authority and default gates

The developer sets autonomy in `project/working-agreement.md`. Options include:

- **Task-gated:** agent completes one numbered task, reports evidence and stops.
- **Increment-gated (efficient default):** developer authorizes a set of tasks; agent implements locally and presents one final review. Merge may be separately authorized.
- **Milestone-gated:** agent completes a bounded, approved work package, including merge only if explicitly granted.

**Always require fresh, explicit authorization** for: changing approved requirements/architecture/feature specs; bypassing security checks; destructive or irreversible data actions; sharing private data; using unknown paid services; deploying production; releasing software; and changes to repository visibility/permissions. Human login/UAC prompts cannot be automated away.

Approval of a *draft* for discussion ≠ approved baseline. Design approval ≠ implementation authorization. Implementation approval ≠ merge/deployment approval unless explicitly bundled. Approval must identify scope and allowed external effects.

## Spec state machine

`Draft → Proposed for review → Approved → (Amendment proposed → Approved new revision or Rejected)`

- An **approved** spec is read-only for the agent until an approved amendment identifies the affected requirements and new behavior.
- Record superseded decisions and rationale in `project/decisions/` or a concise register; don't alter history to make the decision seem inevitable.
- Agent may prepare a candidate diff and impact analysis, but must not apply the amendment to the authoritative baseline without approval.
- For urgent bugs, a temporary mitigation within existing approved behavior can be authorized separately; don't silently alter semantics.

## Controlled amendment format

Use [`templates/change-proposal.md`](../templates/change-proposal.md): trigger, original IDs, new wording or decision, consequences, alternatives, migrations, test updates, rollout/rollback and precise approval requested.

## Stop conditions

Stop before an irreversible action, unexplained security/policy conflict, required permission escalation, uncertain data deletion, significant cost exposure, scope incompatibility or conflicting approved sources. Don't stop for trivial reversible implementation details already within authorization.

Report only the decision needed, options, recommendation and consequence. If work can safely continue in unaffected areas, do so within the existing approved scope.

## Audit without ceremony

For a small project, a short decision row with date/status suffices. For a high-risk product, preserve versioned review artifacts and acceptance records. The goal is **recoverable decisions**, not an exhaustive transcript of every chat.
