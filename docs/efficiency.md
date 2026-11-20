# Engineering efficiency and agent context discipline

**Optimize for useful work per token and elapsed minute—not for fewer tests or weaker answers.**

## Context policy

- One live conversation per increment is a reasonable default; start a new conversation when context becomes burdensome. A tiny checkpoint (`current goal, branch, approved work, blockers, next action`) is enough to resume.
- Read the active task and exact relevant requirements, then inspect symbols/dependencies through bounded search. Avoid dumping the full repo, all test logs, old discussion or completed execution history.
- Maintain a small module/context index **only if repeated rediscovery is costly**; it must not become a parallel source of truth.
- Reuse previously established patterns and the approved decisions, not speculative new infrastructure.
- A single agent is the default. Parallel agents require clear isolation and explicit authorization; they can increase total tokens even if elapsed time falls.
- Keep responses small and stateful. Do not produce long MD reports or permanent log artifacts for routine tasks.

## Execution policy

- Run focused checks while editing. Reserve exhaustive verification for the selected acceptance/merge gate.
- Build portable, deterministic, stack-specific verification wrappers only after a stack is chosen. Scripts handle repetitive inspections; agents read summaries and inspect logs only for failures.
- Avoid repeated clean builds, full test suites, dependency reinstallations, browser downloads, image rebuilds and duplicated remote CI runs.
- Use caches when safe; invalidate correctly. Use bounded retries after diagnosing the failure class.
- Keep local/CI environment parity where material, but don't maintain a duplicate OS/platform test matrix absent a real support requirement.
- For UI-heavy products, avoid premature visual redesign; schedule deliberate review/branding work with actual usage feedback, before release if required.

## Tradeoffs

A **full scan before publishing, authorization test after changing access control, data-migration test after changing schema, or restore drill before release** is not redundant. A failed smoke test cannot be waived because CI is expensive.

Do not impose unrequested usage tracking or arbitrary hard token limits; discuss measurable cost/latency optimizations if users want them. Report what was actually tested, what remains pending and why.
