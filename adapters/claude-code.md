# Using with Claude Code

1. Open the repository root in Claude Code; `CLAUDE.md` points to the universal `AGENTS.md` contract.
2. Paste `prompts/00-start.md` for a new project, or the precise task/increment prompt for ongoing work.
3. Use `docs/context-routing.md` and bounded code searches. Don't copy the entire documentation library into context.
4. Keep tool access least-privileged; let the user complete authentication or approve consequential external actions.
5. Use `prompts/11-handoff.md` when beginning another session. State branch/task/approved scope rather than copying old conversation transcripts.

Tool names, model availability, subagents, and permissions vary by installation; do not assume they exist.
