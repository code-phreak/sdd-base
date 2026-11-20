# Security guidance

This starter contains no service, secrets, or executable application code. When using it to build a product:

- Use unique credentials in ignored local files or an approved secrets manager; never commit keys, tokens, cookies, private certificates, user data, or database backups.
- Scan staged changes and history before first publication; use secret scanning in the selected CI platform where available. A clean scan is not a guarantee—review diffs as well.
- Grant coding agents only the local, repository, account, or cloud permissions needed for the approved task. Authentication and security prompts require the actual user's participation.
- Never disable system security, branch protections, approvals, or checks as a silent workaround.
- Use synthetic or redacted data by default; define privacy, retention, consent, authorization and recovery requirements appropriate to the product.
- Never store confidential project artifacts in a public template repository.

To report a vulnerability in the starter, contact the repository maintainer privately through the security-reporting channel they publish. Do not place exploit details or secrets in public issues.

Project-specific threat modeling and operational guidance: [`docs/security-operations.md`](docs/security-operations.md).
