# Prompt — verify and finalize a change

Review [PR/MR/branch or local change] against approved requirements and the working agreement. I authorize: [REVIEW ONLY / SQUASH-MERGE AFTER PASS].

Check the exact proposed merge content, not only a previously tested branch commit. Confirm coverage, required local/CI results, secrets scans, migrations, user data compatibility, unresolved risks, manual/live acceptance and documentation. Validate the final content again if fixes change it. Do not label pending tests green.

If merge permission is granted and gates pass, squash-merge where supported; verify the primary branch includes the reviewed work, synchronize locally, delete **only safely incorporated** completed feature branches, and stop owned preview processes without deleting persistent data. No deploy/release follows automatically.

If a gate fails or repository protections are unavailable, report the precise issue and safe next action. Never bypass protections. Summarize outcome, tests, merge commit or blocker and remaining acceptance in at most eight lines.
