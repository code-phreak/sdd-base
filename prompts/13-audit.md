# Prompt — cross-project coverage and consistency audit

Follow `AGENTS.md` and approved project specifications. **Audit, don't silently edit or implement.**

Check for: missing/unowned requirement IDs; duplicate/conflicting definitions; untestable acceptance criteria; architecture decisions that contradict approved behavior; task dependency loops; incomplete authorization/tenant/privacy/backup requirements; tests claimed passed without evidence; unowned hosted/manual checks; feature scope crossing MVP exclusions; and gaps between product UI, backend, data and operations.

Give each finding a severity, precise source/reference, recommended correction and impact. Distinguish genuine blockers from reversible implementation defaults. Propose controlled amendments for any approved artifact that must change; do not apply them before approval.

Summarize coverage totals and only meaningful exceptions. If no material issues remain, recommend the next phase gate and explicitly state what it authorizes (and what it does not).
