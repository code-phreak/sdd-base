# Ship better software with an AI agent and a clear specification

**An open, stack-independent Spec-Driven Development (SDD) starter kit** for solo developers and teams. Start with a rough idea, work through decisions with an AI agent, and build through small, verifiable increments—without turning your project into a mountain of documents.

This repository is a **workflow you can build your own project in**, not an application boilerplate. It contains reusable instructions, prompts, examples, and Markdown templates. It does **not** prescribe languages, cloud providers, coding agents, or CI systems. You choose those as part of design.

## From idea to working software

```text
Idea / existing code
       ↓
Guided discovery → product brief → scope / success measures
       ↓
Testable requirements → architecture / key decisions
       ↓
Increment plan → task specifications / verification
       ↓
Agent implements → local checks → reviewed change / merge
       ↓
Hands-on feedback → iteration → deployment / release
```

Human decisions stay in human hands. The agent can do most of the research, writing, implementation, testing, Git operations, and routine upkeep **within an explicitly authorized scope**.

## Start in three steps

1. **Create a new repository from this template** (or extract the ZIP into an empty folder), then open the folder with your preferred AI coding agent.
2. **Copy [`prompts/00-start.md`](prompts/00-start.md)** into the agent's chat. Tell it your idea in plain language—or ask it to interview you.
3. **Answer only the important questions.** The agent proposes a proportionate plan, asks for approval at meaningful gates, and creates project-specific specifications under `project/` before implementation.

You can also start with an existing repository: copy `AGENTS.md`, `docs/`, `prompts/`, and `templates/` into it, then tell the agent to inventory existing behavior before changing code.

**Example first message:**

> Follow `AGENTS.md` and `prompts/00-start.md`. I want to build [your idea]. Use guided multiple-choice questions where helpful. Keep the documentation proportional to complexity. Don't write application code until I approve the plan.

The starter itself needs no installation, dependencies, credentials, or hosted services.

## What changes as your project grows?

| Project size | Planning and control |
|---|---|
| **Small** — script, utility, isolated feature | Short brief, a few testable requirements, concise design, one task list; proceed after approval |
| **Medium** — application or service | Canonical requirements, architecture decisions, feature increments, verification mapping, reviewed changes |
| **Large / sensitive** — multi-team, regulated, expensive to reverse | Stronger threat/privacy analysis, traceability, dependency review, explicit acceptance and operational gates |

SDD is a **quality discipline, not a requirement to create every template**. The agent should recommend the lightest documentation that preserves clear scope, testability, and safe changes.

## An efficient default development cycle

- **Discover & approve:** Resolve consequential requirements and architecture choices before expensive implementation.
- **Implement locally:** One focused branch per increment; small commits per task; targeted tests as the code changes.
- **Validate once at the right boundary:** Comprehensive affected regression, security, and deployment checks before acceptance or merge; rerun after consequential changes.
- **Review & merge:** A PR or equivalent review when supported. Squash-merge and safely delete merged feature branches if authorized.
- **Iterate deliberately:** Capture feedback, propose the smallest coherent change, and keep approved specifications synchronized through change control.

Approvals are configurable: per-task, per-increment, or milestone-based. **Specification changes, credential/security exceptions, destructive actions, and production deployments always require explicit authorization.** A developer may grant an agent authority to merge passing changes for a specific increment.

## Repository map

| Path | Purpose |
|---|---|
| [`AGENTS.md`](AGENTS.md) / [`CLAUDE.md`](CLAUDE.md) | Short agent contracts; [vendor adapters](adapters/README.md) |
| [`prompts/`](prompts/README.md) | Copy-paste prompts for each lifecycle stage |
| [`docs/`](docs/README.md) | Methods, quality standards, approvals, efficiency, security, collaboration |
| [`templates/`](templates/README.md) | Ready-to-use Markdown artifacts, copied only when needed |
| [`examples/`](examples/README.md) | One small, fictional end-to-end example |
| [`project/`](project/README.md) | Your evolving project's specifications and decisions; no application code yet |

Start small: agents should read `AGENTS.md`, [`docs/context-routing.md`](docs/context-routing.md), the *current prompt*, and only the references needed to make the next decision. **Do not preload the entire framework into every chat.**

## Principles

1. **One source of truth.** Approved requirements live in one canonical location; feature docs reference IDs instead of cloning definitions.
2. **Traceable results.** Every requirement has measurable acceptance evidence and an accountable delivery owner.
3. **Explicit decision rights.** Agent proposes; developer approves scope and consequential changes.
4. **Quality without ceremony.** Appropriate checks must run, but not redundantly after every small edit.
5. **Security by default.** Never put secrets in Git, logs, prompts, or sample files. Use least privilege and review external actions.
6. **Real usability matters.** Accessibility, responsive behavior, recovery and hands-on evaluation are considered early, not assumed from automated tests alone.
7. **Small context, high fidelity.** Narrow searches and scripted checks beat repeated repo dumps and huge chat transcripts.
8. **No fictional completion.** Pending, skipped, blocked, tested, approved, deployed, and released are different states.

## License
Licensed under [MIT](LICENSE). Contributions are welcome; see [CONTRIBUTING.md](CONTRIBUTING.md). Security guidance: [SECURITY.md](SECURITY.md).
