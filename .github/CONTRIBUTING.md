# Contributing to DaemonCores

DaemonCores accepts bug reports, design discussions, documentation corrections, and pull requests across its public repositories.

## Choose the correct repository

- Debian bootc packages, base image, or installer: `debian-bootc`
- Proxmox image or host tools: `DaemonCores-VE`
- reusable workflows and composite actions: `DaemonCores-CI`
- phone research, device schema, or probe converter: `DaemonCores-Phone`
- AlmaLinux prototype: `AlmaBuilder`

Cross-repository changes should describe every affected caller and be coordinated before an interface is changed.

## Before opening an issue

Search existing issues and include:

- the repository, commit, image digest, or release artifact involved;
- architecture and deployment method;
- exact reproduction steps;
- expected and observed behaviour;
- relevant logs with credentials and personal data removed;
- whether the problem also occurs in the upstream Debian, Proxmox, AlmaLinux, bootc, or OSTree project.

Do not report security vulnerabilities in a public issue. Follow [SECURITY.md](SECURITY.md).

## Pull requests

1. Create a focused branch from `main`.
2. Keep generated, experimental, and released behaviour clearly separated.
3. Add or update tests for changes to package builds, boot behaviour, manifests, scripts, or workflows.
4. Update documentation in the same pull request when behaviour or interfaces change.
5. Describe validation performed and any path that remains untested.
6. Verify all required status checks before requesting review.

Use imperative, concise commit subjects. Conventional Commit prefixes are welcome but not required unless the target repository says otherwise.

## Documentation standard

Documentation must distinguish among:

- code that exists in the repository;
- behaviour exercised by CI;
- behaviour validated on physical hardware;
- planned or proposed work.

Do not mark a feature complete based only on a design document, schema field, workflow placeholder, or theoretical compatibility.

## Code of conduct and license

Participation is governed by the [Code of Conduct](CODE_OF_CONDUCT.md). Contributions are licensed under the license of the repository receiving them.
