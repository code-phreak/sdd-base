# Using with another coding agent

Give the agent the repository root, then paste:

> Follow `AGENTS.md` and `docs/context-routing.md`. Read only the active project brief, current task and relevant approved requirements. Begin with `prompts/00-start.md` if no project has been initialized. Never infer tool permissions, scope approvals, merge rights or deployment authority.

If your tool can't read files, copy the minimal contract and relevant stage prompt into its context. If it can't run commands or use Git, let it prepare proposed changes and test instructions for a human; it must not claim checks it couldn't execute.
