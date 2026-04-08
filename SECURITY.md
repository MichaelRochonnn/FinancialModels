# Security Policy

## Supported versions

This repository currently maintains the latest state of the `main` branch.

| Version | Supported |
| --- | --- |
| `main` | Yes |
| Older snapshots / copied local variants | Best effort only |

Because this repository primarily contains Codex skills, templates, and documentation rather than a deployed service, the most important security concerns are usually:

- unsafe prompt or workflow instructions,
- accidental leakage of secrets or internal data in examples,
- misleading guidance that encourages unsafe financial or operational decisions,
- instructions that could cause destructive actions when reused in a broader workflow.

## Reporting a vulnerability

Please do **not** open a public GitHub issue for a suspected security problem.

Instead, use one of these channels:

1. Use GitHub's private vulnerability reporting flow for the repository if the "Report a vulnerability" option is available.
2. If that option is not available, contact the repository owner privately through GitHub.
3. If neither path is practical, open a minimal public issue without sensitive details and request a private follow-up channel.

## What to include in a report

Please include as much of the following as possible:

- affected file(s) or skill(s),
- a short description of the issue,
- why it is security-relevant,
- steps to reproduce,
- impact assessment,
- any suggested mitigation or fix.

## Response expectations

The maintainer will try to:

- acknowledge a report within 5 business days,
- assess severity and scope,
- coordinate a fix before broad disclosure when appropriate.

Response times are best effort and may vary depending on maintainer availability.

## Disclosure policy

If a report is confirmed, the preferred path is coordinated disclosure:

1. confirm the issue,
2. prepare a fix or mitigation,
3. publish the fix,
4. disclose enough detail for users to understand whether they are affected.

## Scope notes

This repository is focused on skills and templates. It does not provide live custody of user funds, brokerage functionality, or a production financial platform. Even so, security-minded review is welcome wherever instructions, examples, or workflows could encourage unsafe behavior.
