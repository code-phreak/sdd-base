# Release and iteration

## Release is a distinct decision

A merged increment is not a deployment. A locally complete feature is not automatically production-ready. Use [`templates/release-checklist.md`](../templates/release-checklist.md) and require explicit authorization for hosted deployment, external secrets, real users/data and public releases.

Before releasing, consider:

- Critical functional journeys and nonfunctional budgets demonstrated with the right environment/data.
- Security, privacy, retention, accessibility and dependency review.
- Migration safety, backup/restore exercises, rollback procedure and emergency stop.
- Real integration acceptance, credentials/scopes, quotas, vendor review and recurring cost.
- User documentation, operating runbook, monitoring/alerting and support ownership.
- Manual usability/device review and unresolved known limitations.
- Release artifact provenance, versioning, changelog and explicit go/no-go decision.

Record which checks are passed vs pending; a live-only check cannot be marked complete by a mock. If a release needs an exception, list the risk, mitigation, owner and explicit sign-off.

## Feedback loop

1. Gather observations (bug, friction, performance, request) with reproducible evidence.
2. Classify defect vs requested change vs assumption mismatch.
3. Locate impacted canonical requirements and architecture decisions.
4. For behavior changes, propose an amendment; for defects, implement within the existing approved contract.
5. Group coherent improvements into an increment; specify acceptance and tests.
6. Authorize, implement, review, release and measure. Preserve existing user data/compatibility.

Avoid cycling through many speculative visual patches. Prefer one user-informed experience/design review and cohesive implementation when appropriate.

## Choosing versions

Adopt version semantics based on users and compatibility promises, not arbitrary development increments. SemVer can begin with an explicitly approved first release (e.g. `1.0.0`), but pre-release conventions may differ. Never automatically tag or publish code without approval.
