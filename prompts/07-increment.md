# Prompt — authorize a full increment, local first

I authorize **all approved tasks in increment [INCREMENT-ID]**, in dependency order, **without intermediate task approvals**. The merge permission for this increment is: [NO / YES, only after passing required checks]. No hosted deployment or release is authorized.

Follow `AGENTS.md`, `project/working-agreement.md`, the current increment specs, and `docs/context-routing.md`.

1. Verify baseline/branch state, then create or reuse one scoped local feature branch. Don't rewrite shared history.
2. For each task: load minimal relevant context, implement narrowly, run targeted checks and mandatory local security guards, make a meaningful local commit, and proceed to the next task without an interim report.
3. Do not push intermediate commits or trigger remote CI unless needed for authorized collaboration. Reuse caches/containers; keep logs concise and ignored.
4. When all tasks are done, run the required comprehensive local verification for the increment: applicable regression, integration, contract, browser/device, security, dependency, SDD coverage and recovery tests. Record unavailable live/hosted checks as pending.
5. Scan candidate changes and relevant history before publishing. Push once and create **one PR/MR or equivalent review**. Validate the final proposed merge content with available CI/review checks, avoiding duplicates. If final code changes, rerun the required affected/final validation.
6. **If and only if explicit merge permission above is YES** and all required gates pass, squash-merge where supported, verify incorporation, safely remove completed local/remote branches and synchronize primary branch. Otherwise stop with review link/diff.
7. If a significant contradiction, irreversible change or security failure cannot be resolved within approved scope, stop and ask for the exact needed authorization.

Avoid speculative refactoring, unrelated features, broad historical reads and unnecessary reports. Keep the final response under ten lines: outcome, evidence, pending items, merge/deployment state and next gate. Do not begin the next increment.
