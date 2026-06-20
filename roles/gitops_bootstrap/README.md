# GitOps Role

Installs and manages the OpenShift GitOps (Argo CD) operator, seeds the initial App-of-Apps tree, and wires Vault-backed repository secrets.

## Requirements

None.

## Variables

- `gitops_bootstrap_operator_*`: tune the Subscription (channel, source, starting CSV, approval, extras).
- `gitops_bootstrap_operator_state` / `gitops_bootstrap_argocd_state`: control whether the operator/App-of-Apps exist (default `present`).
- `gitops_bootstrap_repo_templates`: dictionary describing Git credentials to render into secrets; supports `vault_lookup` entries when `gitops_bootstrap_vault_enabled: true`.
- `gitops_bootstrap_vault_enabled`, `gitops_bootstrap_external_secrets_path`, `g_vault_*`: enable HashiCorp Vault lookups for repo passwords and external secret approles.

## Dependencies

None.

## Example Playbook

```yaml
---
- name: Use lit.ocp.gitops_bootstrap
  hosts: all
  become: true
  roles:
    - role: lit.ocp.gitops_bootstrap
```

## License

MIT

## Author

Lightning IT

## Additional Notes

### Usage

```yaml
- hosts: localhost
  gather_facts: false
  roles:
    - role: lit.ocp.gitops_bootstrap
      vars:
        gitops_bootstrap_operator_channel: gitops-1.18
        gitops_bootstrap_operator_state: present
        gitops_bootstrap_repo_templates:
          platform-repo:
            namespace: openshift-gitops
            repo: https://git.example.com/platform.git
            username: git
            password: changeme
```
