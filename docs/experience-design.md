# Experience, accessibility and visual quality

For any user-facing application, define the user journeys and interaction states before assuming a functional backend means the interface is usable.

## Experience requirements

- Define supported device/browser or input modalities, keyboard/screen-reader expectations and responsive constraints.
- Specify critical forms, loading/error/empty states, unsaved edits, undo/recovery and permission-denied behavior.
- Require workflows to expose what changed, what is pending, and which actions are irreversible.
- Capture real user feedback and prioritize friction by severity/frequency, not by visual preference alone.

## Design direction

Before a major redesign, ask for product positioning, tone, audience, brand assets, visual references, accessibility needs, device distribution and no-go examples. Build an approved design brief. Then update component patterns, navigation and responsive behavior coherently rather than styling screens one at a time.

Separate **functional usability** (which should be present from the beginning) from an **optional dedicated brand/visual polish phase**. For projects requiring a polished launch, schedule the visual review after core workflows are testable and before the release gate. Reuse owned source assets only after confirming licensing and provenance, including third-party material.

## Acceptance

Use real browser/device checks, keyboard operation, representative screen sizes, readable content, understandable error recovery and consistent visual states. A screenshot or successful automated test is not a substitute for hands-on user acceptance. Track issues as actionable revisions with their own verification.

Use [`templates/experience-brief.md`](../templates/experience-brief.md) if the project has a significant UI surface.
