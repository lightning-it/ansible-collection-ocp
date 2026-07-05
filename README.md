# ansible-collection-ocp

<!-- BEGIN LIT_SHARED_RELEASE_MODEL -->

[![CI](https://github.com/lightning-it/ansible-collection-ocp/actions/workflows/collection-ci.yml/badge.svg?branch=develop)](https://github.com/lightning-it/ansible-collection-ocp/actions/workflows/collection-ci.yml)
[![Release](https://github.com/lightning-it/ansible-collection-ocp/actions/workflows/collection-publish.yml/badge.svg?branch=main)](https://github.com/lightning-it/ansible-collection-ocp/actions/workflows/collection-publish.yml)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-lit.ocp-blue)](https://galaxy.ansible.com/ui/repo/published/lit/ocp/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

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

<!-- END LIT_SHARED_RELEASE_MODEL -->
Opinionated Ansible roles for Red Hat OpenShift Container Platform: cluster bring-up, day-2 operations and platform services.
