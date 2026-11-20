# Verification without redundant work

Automated checks are evidence, not substitutes for human acceptance. Choose checks according to the change's risk and the approved working agreement.

## Three levels

| Level | When | Expected checks |
|---|---|---|
| **Focused** | During each task | Tests for affected logic and contracts; relevant build/type/lint checks; mandatory local secret guards |
| **Task exit** | Before claiming task complete | Required affected integration, edge/error paths, authorization and regression checks; explicit deferred list |
| **Increment/release gate** | Before merge/acceptance | Complete applicable regression, security, integration, browser/device, recovery, SDD traceability, performance/operations checks |

A small project may use the same quick command at multiple levels; a complex project may have separate suites. **No test is skipped solely because it's expensive if its evidence is required for the current gate.** Record postponed tests and their owner.

## Automation strategy

After the stack is known, generate **project-specific** `test`, `check`, `preview`, `stop`, `status`, and `security` commands/scripts where valuable. Prefer one stable interface and reuse existing tools; this starter intentionally includes no executable scripts.

Checks should:

- Produce deterministic exit codes and small pass/fail summaries, with detailed ignored logs available on demand.
- Select affected tests based on dependencies, not filenames alone; expand scope when uncertain.
- Use isolated synthetic fixtures, repeatable data seeds and cleanup; never erase unowned/persistent data automatically.
- Bound timeouts, retries, resources and concurrency; classify transient vs actual failures before rerunning.
- Cache dependencies and reuse containers/build outputs when safe; rebuild when reproducibility/invalidation demands it.
- Keep essential secret checks mandatory before publication and at CI/review boundaries.

## CI policy

Default to **local-first development**, with a single planned comprehensive CI run against the final proposed merge commit per increment (when the repository supports CI). Avoid duplicate branch-push and PR triggers. Rerun affected checks after fixes; if final validated content changes materially, rerun the required final suite. Account for protected branches and differences in CI plans.

Never automate a merge merely because one check is green if required reviews, tests, or user approval are outstanding.

## Verification dimensions

- **Correctness:** happy path, failure path, boundaries, concurrency, retry/idempotency, preservation of previous state.
- **Contracts:** API, serialized data, imported/exported files, migrations, backwards compatibility.
- **Security:** auth/authz, tenant isolation, input/output sanitization, CSRF where relevant, secret scanning, dependencies, logging privacy.
- **Experience:** keyboard navigation, readable errors, responsive layout, screen-reader considerations, real supported devices when necessary.
- **Operations:** startup/shutdown, readiness, resource/cost limits, backup/restore, rollback and alerts where required.
- **External:** live integrations, permissions, quotas, billing, production deployment. **Mocked checks cannot close real-service acceptance.**

Keep an acceptance ledger recording **pass / fail / pending / blocked / waived with explicit authority**. Do not represent unexecuted checks as green.
