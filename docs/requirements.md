# Requirements and acceptance discipline

## One canonical definition per requirement

Maintain functional requirements in `project/requirements.md` and cross-cutting quality requirements in `project/quality.md` (or combine for Lite projects). Use stable IDs such as `REQ-001`, `SEC-001`, `OPS-001`, `UX-001`; never reassign an ID to a different obligation. Feature specs **reference IDs** and add context/scenarios, rather than redefining the canonical rule.

A good requirement is:

- **Atomic:** one independently verifiable obligation.
- **Behavioral:** describes observable outcome, not an arbitrary implementation choice.
- **Conditional:** describes triggers, actors and preconditions where needed.
- **Precise:** explicit inputs, error behavior, permissions, data effects and boundaries.
- **Verifiable:** acceptance criteria identify evidence, including negative cases.
- **Traceable:** source/rationale, implementation owner, test owner and status.

## EARS-style wording

Use a clear structured pattern without turning every sentence into boilerplate:

- Ubiquitous: “The system shall [observable behavior].”
- Event-driven: “When [event], the system shall [behavior].”
- State-driven: “While [condition], the system shall [behavior].”
- Unwanted behavior: “If [failure or invalid state], the system shall [safe response].”
- Optional: “Where [feature flag or capability is enabled], the system shall [behavior].”

**Example**: “When a user submits a stale edit version, the system shall reject the update without overwriting the current record and shall provide enough information to recover the unsaved change.”

This is superior to “Support editing” or “Use optimistic locking.” The former is ambiguous; the latter specifies a mechanism rather than observable behavior.

## Qualities should have thresholds

Specify performance, reliability, privacy, accessibility, maintainability, cost, operational recovery and portability **with measurement context**. Avoid generic “fast,” “secure” or “scalable.” E.g., define workloads, percentiles, duration, environment and test method. Identify requirements that cannot be locally verified, and the later gate where they will be checked.

## Acceptance mapping

For each requirement, record:

`ID → primary increment/owner → implementation task → test/check → result/evidence → pending external checks`

Cross-cutting requirements may have additional verification links. A demonstration is not final acceptance if a later increment completes the invariant. Explicitly distinguish **Implemented**, **Locally verified**, **Externally verified**, **Accepted**, **Deferred**, and **Blocked**.

## Source reconciliation and change control

Keep original source claims, user decisions and the approved baseline distinguishable. When a later design choice conflicts with a requirement, submit a **controlled amendment** with impact on tests/dependencies. Do not quietly rewrite the approved requirement. See [`approval-and-change-control.md`](approval-and-change-control.md).
