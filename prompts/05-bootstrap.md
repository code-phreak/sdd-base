# Prompt — authorize repository foundation only

I authorize **repository/bootstrap work only**, subject to the approved `project/working-agreement.md` and architecture. Follow `AGENTS.md` and `docs/quality-verification.md`.

- Verify the local repo and permissions; select only the toolchain approved by the project. Build a minimal, working source/test skeleton, reproducible local setup, ignored secrets/config examples, and project-appropriate CI **only if CI/tooling is within authorization**.
- Keep this framework available as reference. Change the top-level README into a **human-readable product/project introduction first**, with contributor/SDD guidance secondary.
- Establish a concise local run/start/stop/verify procedure. Avoid duplicating scripts and generated documentation. Do not depend on a developer's personal OS if the approved target is different.
- Run real smoke/build checks, relevant secret/dependency scans and any required local integration verification. Mark blocked/external checks pending.
- If a Git remote is authorized, create/use private visibility as specified, least privileges, reviewable branch and the permitted PR/CI operations. Never push unscanned secrets or create a public remote accidentally.
- Do **not** implement the first feature, merge, provision production, deploy, call paid APIs or change approved specs unless separately granted.

Finish with the actual commands/results, relevant diff/review location, blockers and the next explicit approval gate. Stop.
