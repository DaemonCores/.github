# ☢️ DaemonCores

---

**DaemonCores** joue sur deux niveaux à la fois :

- **Daemon** — les daemons Linux, ces processus qui tournent en silence dans l'ombre de ton OS
- **Core** — le cœur atomique, *l'atomic* — comme dans Fedora Atomic, AlmaLinux Atomic

---

## Ce qu'on fait ici

Un labo à deux têtes pour expérimenter avec les distros **Atomiques** — les variantes immuables qui nous passent par la tête.

Silverblue, Kinoite, Sericea, Universal Blue, AlmaLinux Atomic, images OCI custom, layers expérimentaux… si ça compile et que ça redémarre pas comme prévu, c'est ici que ça finit.

```
$ rpm-ostree status
● DaemonCores:stable
       Version: ∞ (2025-??-??)
      BaseCommit: cafebabe...
          Layers: trop
```

---

## Stack & terrain de jeu

| Technologie | Rôle |
|---|---|
| `rpm-ostree` / `bootc` | Système de base immuable |
| Fedora Atomic Desktops | Silverblue · Kinoite · Sericea · Onyx |
| AlmaLinux | Variantes RHEL-compatibles |
| Universal Blue / `ublue` | Base pour nos images custom |
| Containerfiles / OCI | Construction des couches |
| `Justfiles` | Automatisation des builds |
| Nix (parfois) | Quand on a envie de souffrir |

---

## Philosophie

> L'OS immuable n'est pas une contrainte — c'est une discipline.

On part du principe qu'un système qui ne peut pas être cassé par `sudo rm -rf` mal placé est un système sur lequel on peut vraiment construire quelque chose. Les layers s'empilent, les commits s'accumulent, les rebases échouent parfois — mais la bombe est stable.

*Jusqu'à ce qu'elle ne le soit plus.*

---

## Contribuer

C'est un labo privé à deux cerveaux pour l'instant. Les issues ouvertes sont les bienvenues si tu as des suggestions, des retours d'expérience ou des idées de builds.

---

<p align="center">
  <sub>DaemonCores — Deux types, trop de distros, zéro regret.</sub><br>
  <sub>⚛️ Atomic by design. Critical by accident.</sub>
</p>
