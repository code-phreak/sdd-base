# Git workflow — platform neutral, review friendly

The starter works with GitHub, GitLab, Bitbucket, self-hosted Git servers or local-only Git. Choose the host in discovery; do not assume a CLI or remote exists.

## Default flow

1. Confirm a clean, synchronized primary branch (often `main`).
2. Create a scoped topic branch from the approved baseline.
3. Develop **locally first**, with meaningful commits per task and targeted checks. Do not publish intermediate changes unless coordination or backup requires it.
4. At increment completion, run full required local verification and a secret scan **before first publication**.
5. Push the completed change and create **one PR/MR or equivalent review**. Trigger necessary final CI once per validated content state; avoid duplicate triggers.
6. After required checks and approval, **squash-merge** where supported. Verify the merged tree incorporates reviewed work.
7. Delete the completed feature branch locally/remotely **only when incorporation is confirmed**, including squash merges (ancestry alone is insufficient).

Retain active branches. Never force-push shared primary branches, overwrite others' work, or delete ambiguous/unmerged branches. Keep private projects private. Use review and access protections where available; note plan limits instead of claiming they exist.

## Permissions

An agent may handle local Git, hosting CLI, branches, PRs and CI automatically **only within explicitly granted authority**. Authentication must be completed by the actual user. Repository creation, visibility changes, merge, branch deletion and hosted deployment are distinct actions; don't infer permission from the ability to run the command.

## Security gates

- Never commit secrets, tokens, local databases, private user content, logs or backup archives.
- Review `.gitignore` and tracked files; an ignore pattern does not remove an already tracked secret.
- Scan candidate changes and relevant Git history before first remote push. If a secret is discovered, stop publication and rotate/revoke as needed; merely deleting it from the latest commit is insufficient.
- CI and local hooks are complementary. Don't assume hooks and optional server features prevent all direct pushes.

## Release tags

Tags and published releases are **separate** from merges. Choose a release policy deliberately (e.g. SemVer `MAJOR.MINOR.PATCH` once actual compatibility promises exist). Never automatically publish a release after an increment merge unless approved.

## Local preview lifecycle

When relevant, let the agent start/restart/stop the project's owned services through reproducible tooling. Bind local previews safely; preserve state unless reset is explicitly authorized; never kill unrelated processes or delete volumes indiscriminately.
