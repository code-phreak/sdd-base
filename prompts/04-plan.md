# Prompt — increments, tasks and coverage

Follow `AGENTS.md`, `docs/planning.md`, and approved requirements/architecture.

1. Propose a coherent sequence of small, demonstrable vertical slices, including early foundations and applicable release-hardening work. Favor early end-to-end value without weakening cross-cutting safeguards.
2. Assign each canonical requirement one primary implementation/acceptance increment, with additional verification references where necessary. Identify gaps and impossible dependencies.
3. For each increment, define `requirements.md` (canonical IDs + acceptance scenarios), `design.md` (scope-specific technical design), and `tasks.md` (ordered, independently verifiable tasks). Keep canonical requirement definitions in their original files.
4. Provide a checkable coverage map and explicit status of features only demonstrated early but finally accepted later.
5. Specify the initial repository bootstrap separately from implementing application features. Define the smallest practical first coding assignment and test/run expectations.
6. Audit all cross-feature dependencies, testing coverage, security requirements, release blockers, and change-control rules before presenting the plan.

Ask me to approve the plan and the relevant **scope of implementation authority**. Do not write product code, provision services or assume approval to merge or deploy.

For Lite projects, combine compatible artifacts and omit increments that add no value.
