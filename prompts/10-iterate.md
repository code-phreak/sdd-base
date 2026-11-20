# Prompt — feedback, defect or change request

I have this feedback: [describe problem/request; provide examples if possible].

Follow `AGENTS.md`, `docs/release-and-iteration.md` and `docs/approval-and-change-control.md`.

1. Reproduce or characterize the observation using targeted evidence; distinguish defect, ambiguous contract, requested behavior change and purely visual preference.
2. Locate impacted canonical requirement IDs, architecture decisions, current tests and user journeys. Propose the smallest correction that solves the underlying problem.
3. For behavior/design changes, prepare a controlled amendment with impacts and approval request. For defects already covered by an approved contract, propose a narrow implementation task and regression test.
4. Prioritize by user impact, severity, data/security risk and dependencies. Suggest batching compatible feedback to avoid repeated iterations.
5. Ask for explicit authorization before altering approved specifications, implementing a new feature, merging or deploying. Use local-first targeted verification once authorized.

Return a concise diagnosis, recommended change, tests, risks and next decision.
