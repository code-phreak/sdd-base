# Working agreement — [Project]

**Status:** Draft · **Approved by/date:** [pending]

## Collaboration mode
- **Project scale:** [Lite / Standard / Rigorous]
- **Agent(s):** [preferred agent and tooling; default single agent]
- **Developer role:** [product owner / reviewer / team]
- **Question mode:** [free text / short recommended-option surveys / hybrid]
- **Response style:** [concise, decision-focused; preferred number of questions]
- **Documentation budget:** [minimal artifacts / standard / formal controls]

## Authorization model
- **Implementation:** [one task / one increment / named milestone per explicit approval]
- **Merge:** [separate approval / expressly allowed within named increment after required checks]
- **Hosted deployment/release:** Explicit approval each time.
- **Approved spec changes:** Proposed amendment and human approval before application.
- **Destructive operations, security exceptions, private-data transfer, paid APIs, repo visibility:** Explicit approval.

## Repository / environment
- **Git host:** [none / platform]; **primary branch:** [main]; **remote visibility:** [private/public]
- **Local-first?** [yes/no]; **review mechanism:** [PR/MR/diff]; **merge/cleanup:** [squash and safe delete / other]
- **Build/test OS/platform:** [project decision, not assumed]; **preview lifecycle:** [commands or pending]

## Verification cadence
- **During tasks:** Targeted tests + required guards.
- **At review:** [affected/full regression, security, integration, UI, SDD].
- **External/device/hosted checks:** Record as pending until executed.
- **Remote CI:** [at final increment boundary by default / custom].

## Security and costs
- **Sensitive data classification and restrictions:** [data/roles]
- **Secret storage:** [ignored local file or managed store]
- **Spending authority/budget:** [limits; no unapproved paid operations]

## Escalation and stop criteria
[Conflicts, security gaps, unknown spending, irreversible actions, permissions, required sign-off.]
