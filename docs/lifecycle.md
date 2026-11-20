# Lifecycle and phase gates

The sequence below is adaptable. A one-file utility may combine steps; a sensitive service may require more thorough evidence.

| Phase | Deliverable | Exit condition |
|---|---|---|
| 0. Intake | Idea/existing-system inventory, objectives, constraints, unknowns | User confirms intent and authority to inspect sources |
| 1. Discover | Brief, audience, workflows, scope boundaries and risks | Material product choices resolved or explicitly deferred |
| 2. Specify | Canonical requirements, quality properties, acceptance scenarios | Testable baseline approved for design |
| 3. Design | Components, data flow, contracts, alternatives, ADRs | Consequential architecture choices approved |
| 4. Plan | Increments, task specs, dependencies, requirement-to-verification allocation | Implementation scope and autonomy approved |
| 5. Bootstrap | Minimal repo, build/test scaffolding, secrets exclusions, local runbook | Foundation runs; no unapproved feature work |
| 6. Implement | Focused code/tests/docs per authorized task or increment | Targeted verification, honest pending status |
| 7. Accept | Final applicable integration/security/UX checks, reviewable changes | Approved merge/release decision |
| 8. Deploy | Controlled environments, backups/recovery, release artifacts | Separately authorized deployment and operational acceptance |
| 9. Iterate | Feedback, defects, revised specifications, new increments | Controlled amendments and next approved work |

**Approval does not imply an automatic next phase**. Approval of requirements for architecture is not approval to write application code. An increment implementation approval is not permission to deploy or release. Scope approval can cover a task, a series of tasks, or an entire increment; record it in the working agreement/current chat.

## Proportional tracks

- **Lite:** A single brief and small set of measurable requirements; short design and task checklist; explicit implementation and release gates. Suitable when changes are reversible and integrations limited.
- **Standard:** Separate canonical requirements, quality requirements, key architectural decisions, feature specs and coverage mapping.
- **Rigorous:** Add threat model, formal source coverage, risk review, migration strategy, disaster-recovery exercises, nonfunctional budgets and review sign-offs as justified.

Choose the **smallest track that makes risk explicit**. Escalate if handling sensitive information, regulated workflows, large financial impact, multi-account boundaries, difficult migrations or high public exposure.

## Work already underway

When adopting the kit for an existing codebase, inspect actual behavior and tests before drafting replacement specs. Identify what's *observed*, *claimed*, *desired*, and *approved*; don't silently relabel current behavior as compliant. Establish a baseline and select one narrow next increment.

## Scope control

Separate **MVP/release scope**, **later possibilities**, and **out-of-scope**. Keep aspirational designs in a clearly non-binding location; agents must not use them as authorization for features. Preserve acceptance and implementation provenance only to the extent useful for future development, maintenance or compliance.
