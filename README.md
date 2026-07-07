# ansible-collection-ocp

<!-- BEGIN LIT_SHARED_RELEASE_MODEL -->

## Release and Quality Model

This repository follows the Lightning IT shared release and quality model.

See [RELEASE.md](./RELEASE.md) for:

- branch and release flow
- required quality checks
- test matrix
- release evidence
- artifact publishing
- supported repository-specific release behavior

Repository classification: **Ansible Collection**.
Required test profiles: `pre-commit, lint, light, molecule-light, molecule-heavy-incus, release-validation`.
Publishing targets: `github-release, ansible-galaxy`.

## Supported and Tested Platforms

| Platform / Product | Status | Validation |
|---|---:|---|
| ubuntu-latest | Supported | Molecule / Incus |
| rhel-9 | Supported | Molecule / Incus |
| rhel-10 | Supported | Molecule / Incus |
| ansible-core | Tested where applicable | Molecule / Incus |
| openshift-client | Tested where applicable | Molecule / Incus |
| incus | Tested where applicable | Molecule / Incus |

<!-- END LIT_SHARED_RELEASE_MODEL -->

<!-- BEGIN LIT_QUALITY_BADGES -->

[![CI](https://github.com/lightning-it/ansible-collection-ocp/actions/workflows/collection-ci.yml/badge.svg?branch=develop)](https://github.com/lightning-it/ansible-collection-ocp/actions/workflows/collection-ci.yml)
[![Latest Release](https://img.shields.io/github/v/release/lightning-it/ansible-collection-ocp?sort=semver)](https://github.com/lightning-it/ansible-collection-ocp/releases/latest)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/lightning-it/ansible-collection-ocp/badge)](https://scorecard.dev/viewer/?uri=github.com/lightning-it/ansible-collection-ocp)
[![Ansible Galaxy](https://img.shields.io/ansible/collection/v/lit/ocp?label=Ansible%20Galaxy)](https://galaxy.ansible.com/ui/repo/published/lit/ocp/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

<!-- END LIT_QUALITY_BADGES -->

`lit.ocp` is a Lightning IT Ansible Collection for reusable automation across ansible-core, openshift-client, incus.

## Features

- Reusable roles, modules, plugins, or playbook building blocks for Lightning IT automation.
- Collection sanity validation and Molecule scenarios where configured.
- GitHub Release evidence and Ansible Galaxy publishing where enabled.

## Included Content

| Content Type | Location |
|---|---|
| Roles | `roles/` |
| Plugins and modules | `plugins/` where present |
| Documentation | repository docs and Ansible Galaxy |

## Requirements

- Ansible Core compatible with the tested release matrix.
- Supported products: `ansible-core, openshift-client, incus`.

## Installation

```bash
ansible-galaxy collection install lit.ocp
```

## Quick Start

```yaml
- hosts: all
  gather_facts: true
  roles: []
```

## Examples

See repository examples, role documentation, and release evidence for validated scenarios.

## Documentation

- [Ansible Galaxy](https://galaxy.ansible.com/ui/repo/published/lit/ocp/)
- [RELEASE.md](./RELEASE.md)
- [TESTING.md](./TESTING.md)
- [SECURITY.md](./SECURITY.md)

Opinionated Ansible roles for Red Hat OpenShift Container Platform: cluster bring-up, day-2 operations and platform services.

## Security

See [SECURITY.md](./SECURITY.md) for supported versions and vulnerability reporting.

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for contribution and review expectations.

## License

See [LICENSE](./LICENSE).

<!-- BEGIN LIT_RELEASE_QUALITY_MODEL -->

## Release and Quality Model

This repository follows the Lightning IT shared release and quality model.
The README shows the current supported and tested matrix.
Exact per-version validation proof is stored with each GitHub Release as `release-evidence.md` and `release-evidence.json`.
Releases are created from the protected `main` branch after a reviewed `develop -> main` release promotion.
Collection releases validate collection sanity, Molecule scenarios, build integrity, and Ansible Galaxy publishing where enabled.

See:

- [RELEASE.md](./RELEASE.md)
- [TESTING.md](./TESTING.md)
- [GitHub Releases](../../releases)

Repository classification: **Ansible Collection**.
Required test profiles: `pre-commit, lint, light, molecule-light, molecule-heavy-incus, release-validation`.
Publishing targets: `github-release, ansible-galaxy`.

<!-- END LIT_RELEASE_QUALITY_MODEL -->

<!-- BEGIN LIT_COMPATIBILITY_MATRIX -->

## Compatibility Matrix

| Collection Version | Platform | Product | Validation |
|---|---|---|---|
| Latest release | ubuntu-latest | ansible-core, openshift-client, incus | See release evidence |
| Latest release | rhel-9 | ansible-core, openshift-client, incus | See release evidence |
| Latest release | rhel-10 | ansible-core, openshift-client, incus | See release evidence |

| Scenario | Test Type | Validation |
|---|---|---|
| collection-sanity | Collection sanity | See release evidence |
| molecule-light | Molecule light | See release evidence |
| molecule-heavy-incus | Heavy Incus | See release evidence |
| galaxy-build | Galaxy build/publish | See release evidence |

Validation proof for each released version is stored in the corresponding GitHub Release evidence.

<!-- END LIT_COMPATIBILITY_MATRIX -->

## Release Evidence

Every released version includes immutable release evidence attached to the corresponding GitHub Release.
The evidence records:

- tested matrix combinations
- GitHub Actions run links
- artifact references
- publish status
- security scan status

See [GitHub Releases](../../releases), [RELEASE.md](./RELEASE.md), and [TESTING.md](./TESTING.md) for the release process and validation model.
