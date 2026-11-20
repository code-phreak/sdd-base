# Worked SDD conversation — a small command-line utility

This **fictional** example demonstrates the *Lite track* without teaching agents to skip important decisions. The same pattern scales to services and multi-team products.

## 1. Idea and adaptive discovery

Developer: “I often receive badly formatted JSON files. I want a command-line utility to validate and pretty-print them.”

Agent summarizes the outcome, then asks **only missing consequential choices**:

- Q1. Input: **A★** file paths and stdin; B files only; C pasted interactive text.
- Q2. Invalid JSON: **A★** nonzero exit code and line/column diagnostic; B silently repair; C ignore invalid files.
- Q3. Output: **A★** stdout by default, explicit `--output` to write files; B overwrite originals; C always create a new file.

Developer: “All recommended. No network or telemetry. Cross-platform.”

Agent writes a short draft brief and asks for approval. It does **not** independently choose a programming language or start coding.

## 2. Canonical requirements

`REQ-001`: When supplied with valid JSON via file or stdin, the utility shall emit equivalent pretty-printed JSON to stdout unless an explicit output path is provided.

`REQ-002`: When supplied with invalid JSON, the utility shall exit nonzero, identify the failure location where possible, and leave input files unchanged.

`REQ-003`: The utility shall not make network requests or collect usage telemetry.

`QUAL-001`: The utility shall run on [explicitly selected supported targets]; exact targets require approval.

Agent proposes acceptance: valid object, valid array, stdin, invalid token, empty input, read-only file, file write failure, output path collision, no network use. Developer approves the baseline **for design only**.

## 3. Architecture, tasks and authorization

Agent proposes a small CLI architecture: parser → validated in-memory value → formatter → output writer. It compares one reasonable runtime/library approach with an alternative, then requests a technical decision. No microservices, DB, cloud provider, or mandatory CI platform are proposed.

Agent proposes one increment and three tasks:

1. `T01-01`: CLI/input and predictable exit codes; targeted parser tests.
2. `T01-02`: formatting/output destination and non-overwrite safeguards; error-path tests.
3. `T01-03`: integration checks, help text and cross-platform verification.

Developer authorizes the increment, but not release publication.

## 4. Efficient development and review

Agent uses a local feature branch, relevant source and task references, and targeted checks while implementing. It commits task outcomes locally and does not push each task to trigger remote CI.

At increment completion, it runs the agreed full verification once, checks for secrets, then opens one reviewable PR/MR. The developer approves squash merging. The agent verifies that reviewed changes are incorporated and safely deletes the completed branch. Publication of a binary/package **requires separate release approval**.

## 5. Feedback and controlled change

A tester observes that the utility handles invalid UTF-8 poorly. The agent checks whether the approved invalid-input requirement already covers it. If yes, it proposes a bug fix with a regression test; if not, it submits a precise requirement amendment before changing behavior.

**Lessons:** few questions, testable outcomes, one source of truth, proportional design, meaningful approval gates, local-first checks, honest external verification, and no invented completion.
