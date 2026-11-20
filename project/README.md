# Project workspace — not yet initialized

Your agent will establish a project here after discovery and approval. **This file is not a specification and authorizes no implementation.**

Typical structure (adapt to project complexity):

```text
project/
  brief.md                    # outcome, audience, scope, success
  working-agreement.md        # autonomy, approvals, verification, repo policy
  requirements.md             # single canonical functional baseline
  quality.md                  # measurable cross-cutting properties
  architecture.md             # key technical design and boundaries
  decisions/ADR-0001-*.md     # consequential, approved architecture decisions
  plan.md                     # increments, demos, dependencies
  coverage.md                 # requirement → owner → tests/evidence
  increments/<id>-<slug>/
    requirements.md           # references canonical IDs, scenarios
    design.md                 # implementation design
    tasks.md                  # atomic tasks and verification
  changes/                    # proposed amendments before approval
  validation/                 # reviewed outcomes and pending checks
  release/                    # deployment and release records
```

For a small project, combine compatible documents and omit unnecessary folders. **Do not duplicate canonical requirement text across feature files.** Keep approved artifacts stable; record proposals separately before applying changes.

Application source, generated tests and CI belong in project-appropriate locations created only after authorization.
