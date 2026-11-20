# Plan increments and tasks for evidence, not paperwork

## Increment design

Prefer **vertical slices** that demonstrate an increasingly complete user outcome. Establish foundational cross-cutting controls early, but avoid months of invisible infrastructure work before the first meaningful demo.

Each increment has:

- Scope, excluded behavior, primary requirement IDs, dependencies and success criteria.
- A demonstrable outcome or meaningful internal contract.
- Task ordering, shared-component risks and test/fixture strategy.
- Acceptance criteria for what becomes final **now** vs what later increments must finish.
- A clear human authorization level for implementation and final merge.

## Task design

Tasks should be small enough to understand and validate in isolation, without imposing arbitrary file-count limits. Define an output contract, impacted modules, requirement IDs, implementation steps and explicit test cases. Prefer test-first for logic and bug fixes where practical. Reserve combined tasks for changes requiring atomic coordination.

**Don't generate implementation tasks before architecture constraints are known.** Tasks can be updated under change control if a measured issue makes a different sequence safer.

## Cross-increment coverage

Use [`templates/coverage.md`](../templates/coverage.md) to allocate each canonical requirement to exactly one **primary acceptance owner** and optional dependent rechecks. Guard against gaps, duplicates and old requirements that became invalid under new decisions.

A realistic first milestone may use synthetic inputs and a fully functioning output, while live integration, advanced controls and production readiness arrive later. Mark the difference rather than claiming an early demo satisfies the full product.

## Build-versus-buy and cost

Record recurring infrastructure/API cost assumptions, privacy/sensitivity implications, license constraints, and scaling thresholds. Use ranges and measurement plans when prices or consumption are uncertain. Never treat an estimate as a tested budget guarantee.

## Implementation gate

Before an agent begins, confirm the approved scope, relevant specs, branching policy, verification boundary, allowed tool permissions, permitted external effects, and stop condition. Use [`prompts/05-bootstrap.md`](../prompts/05-bootstrap.md), [`prompts/06-task.md`](../prompts/06-task.md) or [`prompts/07-increment.md`](../prompts/07-increment.md).
