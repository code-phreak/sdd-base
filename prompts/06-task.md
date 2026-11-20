# Prompt — authorize one implementation task

I authorize **only task [TASK-ID]** in increment [INCREMENT-ID], under the approved specification and working agreement. Follow `AGENTS.md`.

- Read only the task, its requirement IDs, directly relevant architecture/design and affected code. Don't reload unrelated specs or historical chat.
- Implement the smallest correct change, including happy/error/security tests and relevant documentation. Preserve behavior and data contracts outside the authorized scope.
- Run targeted affected checks and required local security checks; preserve detailed ignored logs and report concise outcomes. Do not claim deferred checks passed.
- Commit on the existing increment branch if authorized. Do not push/trigger comprehensive CI prematurely when using local-first mode.
- If a conflicting approved requirement or material security issue appears, prepare the smallest change proposal and stop that portion. Never silently rewrite approved specs.
- Do not start another task, merge, deploy, incur external cost or publish credentials.

Report changes, tests, actual pending checks, blockers and next task. **Stop after this task.**
