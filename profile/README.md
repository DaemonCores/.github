# DaemonCores

DaemonCores develops transactional Linux systems built and distributed as OCI images. The current work centres on bringing the bootc/OSTree model to Debian, using it as a base for an atomic Proxmox VE host, and maintaining the CI required to build, test, sign, and publish those systems.

The organization started as a proof of concept. It is now being developed as an active engineering project, with repository status documented explicitly rather than implied by the organization name.

## Projects

| Repository | Role | Status |
| --- | --- | --- |
| [`debian-bootc`](https://github.com/DaemonCores/debian-bootc) | Debian 13 bootc/OSTree base image, custom Debian packages, installer media, and boot tests | Active development |
| [`DaemonCores-VE`](https://github.com/DaemonCores/DaemonCores-VE) | Transactional Proxmox VE image built on `debian-bootc` | Active development |
| [`DaemonCores-CI`](https://github.com/DaemonCores/DaemonCores-CI) | Reusable GitHub Actions workflows and composite actions shared by the image repositories | Active infrastructure |
| [`DaemonCores-Phone`](https://github.com/DaemonCores/DaemonCores-Phone) | Research branch for a Debian/bootc smartphone system and a schema-driven device pipeline | Early implementation |
| [`AlmaBuilder`](https://github.com/DaemonCores/AlmaBuilder) | Small AlmaLinux bootc image and net-install ISO reference | Prototype |

## What is implemented

- Debian packages for bootc, OSTree, composefs, bootupd, the boot stack, first-boot setup, and project-specific host services.
- OCI image builds with architecture-specific jobs, image signing, content-aware rebuilds, and multi-architecture manifest publication.
- QEMU/KVM boot tests that install an image onto a virtual disk and validate the running system over SSH before publication.
- Online and offline installer media generated from the published image.
- A Proxmox VE layer with bootc-aware networking, storage, firewall, memory, power, cooling, and container tooling.
- A reusable, manifest-driven package and image pipeline shared across repositories.

## Engineering model

The operating system is treated as a versioned image rather than a host assembled by repeated in-place package operations:

1. source packages and project overlays are built into signed Debian repositories;
2. a Containerfile assembles the operating-system image;
3. the image is installed and booted under QEMU for runtime validation;
4. successful builds are published to GHCR and signed;
5. installer artifacts are produced from the published image.

The individual repositories document their supported paths, current limitations, build inputs, and required credentials. Interfaces that are still being validated are labelled as such instead of being presented as released functionality.

## Contributing

Issues and pull requests are welcome. For changes that affect image format, package manifests, boot behaviour, or shared CI interfaces, open an issue first so the design can be discussed across the affected repositories.

Security reports should follow the private reporting process described in the organization-wide [`SECURITY.md`](https://github.com/DaemonCores/.github/blob/main/.github/SECURITY.md).
