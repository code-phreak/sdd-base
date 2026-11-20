# [Project] — Canonical quality requirements

**Status:** Draft · **Baseline:** [pending]

For each applicable dimension, specify test workload/environment, measurable threshold, failure behavior and verification stage. Do not invent thresholds: propose and approve them.

| ID | Dimension | The system shall... | Threshold / environment | Test / stage | Status |
|---|---|---|---|---|---|
| QUAL-001 | Performance | [measurable response] | [workload, percentile, bound] | [measurement] | Proposed |
| SEC-001 | Access control | [prevent unauthorized access] | [roles, isolation] | [negative tests] | Proposed |
| OPS-001 | Recovery | [restore service/data safely] | [RPO/RTO or justified equivalent] | [restore drill] | Proposed |
| UX-001 | Accessibility | [interaction outcome] | [supported devices/standard] | [keyboard/device checks] | Proposed |

Consider only relevant risks: reliability, durability, privacy, compatibility, security, operability, maintainability, scalability, cost, accessibility, localization, support. Mark any real-host/device/API requirement with its future acceptance gate.

**Approval requested:** Quality baseline for design; not implementation.
