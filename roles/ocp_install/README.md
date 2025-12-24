# ocp_install (facade)

Front-door role for installing OpenShift in the `lit.ocp` collection. Dispatches to method-specific roles based on `ocp_install_method`.

## Variables

- `ocp_install_method`: installation approach; supported values: `upi`, `agent` (default: `agent`).
- `ocp_install_cluster_name`: cluster name (common input).
- `ocp_install_base_domain`: base domain for cluster DNS.
- `ocp_install_pullsecret`: pull secret content.
- `ocp_install_ssh_pub_keys`: list of SSH public keys to embed.

Method-specific variables live in the implementation roles:
- `ocp_install_upi_*` for UPI
- `ocp_install_agent_*` for agent-based installs

## Examples

```yaml
- name: Install OCP via UPI
  hosts: localhost
  connection: local
  gather_facts: false
  roles:
    - role: lit.ocp.ocp_install
      vars:
        ocp_install_method: upi
        ocp_install_cluster_name: demo-ocp
        ocp_install_base_domain: dev.l-it.io
        # plus ocp_install_upi_* vars
```

```yaml
- name: Install OCP via agent-based flow
  hosts: localhost
  connection: local
  gather_facts: false
  roles:
    - role: lit.ocp.ocp_install
      vars:
        ocp_install_method: agent
        ocp_install_cluster_name: demo-ocp
        ocp_install_base_domain: dev.l-it.io
        # plus ocp_install_agent_* vars
```
