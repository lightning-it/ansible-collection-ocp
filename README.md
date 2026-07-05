# ansible-collection-ocp

<!-- BEGIN LIT_QUALITY_BADGES -->

[![CI](https://github.com/lightning-it/ansible-collection-ocp/actions/workflows/collection-ci.yml/badge.svg?branch=develop)](https://github.com/lightning-it/ansible-collection-ocp/actions/workflows/collection-ci.yml)
[![Latest Release](https://img.shields.io/github/v/release/lightning-it/ansible-collection-ocp?sort=semver)](https://github.com/lightning-it/ansible-collection-ocp/releases/latest)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/lightning-it/ansible-collection-ocp/badge)](https://scorecard.dev/viewer/?uri=github.com/lightning-it/ansible-collection-ocp)
[![Ansible Galaxy](https://img.shields.io/ansible/collection/v/lit/ocp?label=Ansible%20Galaxy)](https://galaxy.ansible.com/ui/repo/published/lit/ocp/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

<!-- END LIT_QUALITY_BADGES -->

<!-- BEGIN LIT_COMPATIBILITY_MATRIX -->

## Compatibility Matrix

| Collection Version | Role/Scenario | Platform | Product | Test Type | Validation |
|---|---|---|---|---|---|
| Current release | collection-sanity | ubuntu-latest | ansible-core, openshift-client, incus | Collection sanity | See GitHub Release evidence |
| Current release | molecule-light | ubuntu-latest | ansible-core, openshift-client, incus | Molecule light | See GitHub Release evidence |
| Current release | molecule-heavy-incus | ubuntu-latest | ansible-core, openshift-client, incus | Heavy Incus | See GitHub Release evidence |
| Current release | galaxy-build | ubuntu-latest | ansible-core, openshift-client, incus | Galaxy build/publish | See GitHub Release evidence |
| Current release | collection-sanity | rhel-9 | ansible-core, openshift-client, incus | Collection sanity | See GitHub Release evidence |
| Current release | molecule-light | rhel-9 | ansible-core, openshift-client, incus | Molecule light | See GitHub Release evidence |
| Current release | molecule-heavy-incus | rhel-9 | ansible-core, openshift-client, incus | Heavy Incus | See GitHub Release evidence |
| Current release | galaxy-build | rhel-9 | ansible-core, openshift-client, incus | Galaxy build/publish | See GitHub Release evidence |
| Current release | collection-sanity | rhel-10 | ansible-core, openshift-client, incus | Collection sanity | See GitHub Release evidence |
| Current release | molecule-light | rhel-10 | ansible-core, openshift-client, incus | Molecule light | See GitHub Release evidence |
| Current release | molecule-heavy-incus | rhel-10 | ansible-core, openshift-client, incus | Heavy Incus | See GitHub Release evidence |
| Current release | galaxy-build | rhel-10 | ansible-core, openshift-client, incus | Galaxy build/publish | See GitHub Release evidence |

Validation proof for each released version is stored in the corresponding GitHub Release evidence.

<!-- END LIT_COMPATIBILITY_MATRIX -->

<!-- BEGIN LIT_RELEASE_QUALITY_MODEL -->

## Release and Quality Model

This repository follows the Lightning IT shared release and quality model.
The README shows the current supported and tested matrix.
Exact per-version proof is stored with every GitHub Release as `release-evidence.md` and `release-evidence.json`.

See:

- [RELEASE.md](./RELEASE.md)
- [TESTING.md](./TESTING.md)
- [GitHub Releases](../../releases)

Repository classification: **Ansible Collection**.
Required test profiles: `pre-commit, lint, light, molecule-light, molecule-heavy-incus, release-validation`.
Publishing targets: `github-release, ansible-galaxy`.

Release evidence records the exact GitHub Actions run, validated matrix rows, built artifacts, publish result, and security status for each release.

<!-- END LIT_RELEASE_QUALITY_MODEL -->

Opinionated Ansible roles for Red Hat OpenShift Container Platform: cluster bring-up, day-2 operations and platform services.
