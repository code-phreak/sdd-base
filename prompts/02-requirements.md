# Prompt — canonical requirements and acceptance

Follow `AGENTS.md`, `docs/requirements.md`, and the approved `project/brief.md`. Do not rewrite the brief without asking.

1. Derive atomic, observable, independently verifiable functional and quality requirements. Use stable IDs and EARS-style conditions where helpful.
2. Keep requirement text canonical in `project/requirements.md` / `project/quality.md` (or an agreed Lite equivalent). Note origin, actor, preconditions, data effects, negative paths and precise success evidence.
3. Define measurable quality expectations proportional to project risk. Mark uncertain numerical thresholds as proposed, not approved.
4. Propose acceptance scenarios covering success, invalid inputs, concurrency, permissions, failure recovery, and relevant accessibility/operations.
5. Reconcile the source brief with every requirement. Show omitted source obligations, scope creep, contradictions, and unresolved decisions. Do not silently fix source meaning.
6. Request explicit approval of the baseline **for architecture/design use only**. Preserve ID stability and do not generate implementation code.

Use `templates/requirements.md`, `templates/quality.md`, and `templates/acceptance-log.md` as needed. Keep output compact; do not create unused templates or unnecessary duplicate summaries.
