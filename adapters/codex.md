# Using with Codex

1. Open the repository folder as the Codex project. Start with `prompts/00-start.md` or the current stage-specific prompt.
2. `AGENTS.md` is the short operating contract; use `docs/context-routing.md` to avoid loading unrelated materials.
3. Let Codex inspect the approved task and relevant code, not the whole requirements corpus on each turn.
4. Grant local Git/tool use to the extent appropriate; repository, cloud, paid API and production actions still require explicit authorization.
5. For long increments, compact or start a fresh conversation with `prompts/11-handoff.md`. Preserve secrets and handoff notes outside tracked files.

Do not assume a particular model, reasoning level, approval UI, GitHub integration or shell capability; configure those in the project working agreement if available.
