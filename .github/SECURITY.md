# Security policy

## Reporting a vulnerability

Do not open a public issue for a suspected vulnerability.

Use GitHub private vulnerability reporting in the affected repository when it is available. If the affected repository is unclear or private reporting is unavailable, email `guillou.gabriel@gmail.com` with the subject `DaemonCores security report`.

Include the affected repository and revision, impact, reproduction steps, relevant configuration, and any proof of concept that can be shared safely. Remove unrelated credentials and personal data.

## Supported state

DaemonCores is under active development and does not currently publish a versioned long-term-support channel. Security work targets the current default branch and the most recent artifacts produced from it.

Older images, package repositories, installer media, and commits should be treated as unsupported unless a repository explicitly states otherwise.

## Scope

Reports are especially useful for:

- image or package supply-chain compromise;
- privilege escalation introduced by project scripts or services;
- unsafe installer or disk-selection behaviour;
- signature, key, or repository verification bypasses;
- credential exposure in workflows or build logs;
- isolation failures in Proxmox, OSTree, composefs, or container integration caused by project code.

Upstream vulnerabilities that reproduce without DaemonCores modifications should also be reported to the relevant upstream project.

## Disclosure

Reports are handled on a best-effort basis. The maintainer will confirm the affected component, coordinate a fix and advisory when appropriate, and agree on disclosure timing with the reporter. Do not assume a fixed response or release deadline for this community-maintained project.
