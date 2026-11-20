# Prompt — compact context checkpoint for a new agent chat

Prepare a **small, private, Git-ignored** handoff checkpoint for the next conversation, then stop. Do not implement or alter remote state.

Capture only: current phase/approved scope; branch + HEAD + worktree status; relevant canonical specs and source entry points; completed/remaining task IDs; outstanding blockers and deferred verification; next allowed action and stop condition. Cap at approximately 300–500 words.

Place it under an ignored local directory (for example `.tmp/agent-handoff.md`) without secrets, private user data, historical chat, or copied specifications. Confirm that the path is ignored and never stage/commit it. If no filesystem access exists, give a short copyable checkpoint in chat instead.

**New chat opening:** “Follow `AGENTS.md` and read only `.tmp/agent-handoff.md` plus the active task/spec. Verify Git state; don't reconstruct earlier conversations. Continue only within the recorded authorization.”
