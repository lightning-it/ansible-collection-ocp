===================================================
Lightning IT Collection Release Notes Release Notes
===================================================

.. contents:: Topics

v1.9.0
======

Minor Changes
-------------

- gitops_bootstrap - Add Vault secret-path support for repository credential templates while retaining complete lookup-term compatibility.
- install_agent - Add an option to reuse staged OpenShift client tools instead of downloading them again.

Bugfixes
--------

- Normalize GitOps bootstrap Vault secret lookups to the collection-compatible lookup-term format and document the required ``<path>:<field>`` target.
- Remove the managed Argo CD trusted TLS certificate ConfigMap when no TLS certificates are configured or the GitOps operator is removed, preventing stale trust configuration.
- gitops_bootstrap - Honor the configured App-of-Apps repository URL without appending a fixed suffix.
- gitops_bootstrap - Support Vault secret paths and trusted TLS certificates while honoring the configured App-of-Apps repository URL.
- install_agent - Render the AgentConfig NTP field with the casing required by the OpenShift API.

v1.8.0
======

Minor Changes
-------------

- collection_tooling - Synchronize the centrally managed Renovate policy and guarded automation workflows.

Bugfixes
--------

- collection_tooling - Dispatch releases through protected main, use the configured Galaxy environment secret, trust lint-version metadata from the managed image, and ignore generated Python and collection-install artifacts.

v1.7.0
======

Minor Changes
-------------

- docs - Apply the shared enterprise README structure.
- docs - Consolidate generated governance metadata and license policy on shared-assets-lit.
- release_model - Add managed compatibility matrix documentation and structured release evidence fields.

v1.6.0
======

Minor Changes
-------------

- lit.ocp - Verify automated collection release workflow after final back-sync race fix.

v1.5.0
======

Minor Changes
-------------

- lit.ocp - Verify automated collection release workflow cycle 2.

v1.4.0
======

Minor Changes
-------------

- lit.ocp - Verify automated collection release workflow cycle 1.
