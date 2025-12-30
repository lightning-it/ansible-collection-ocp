# install (facade)

Front-door role for installing OpenShift in the `lit.ocp` collection. Dispatches to method-specific roles based on `install_method`. Legacy `ocp_install_*` inputs remain accepted.

## Variables

- `install_method`: installation approach; supported values: `upi`, `agent` (default: `agent`).
- `install_cluster_name`: cluster name (common input).
- `install_base_domain`: base domain for cluster DNS.
- `install_pullsecret`: pull secret content.
- `install_ssh_pub_keys`: list of SSH public keys to embed.

Method-specific variables live in the implementation roles:
- `install_upi_*` for UPI (legacy `ocp_install_upi_*` still accepted)
- `install_agent_*` for agent-based installs

## Examples

```yaml
- name: Install OCP via UPI
  hosts: localhost
  connection: local
  gather_facts: false
  roles:
    - role: lit.ocp.install
      vars:
        install_method: upi
        install_cluster_name: demo-ocp
        install_base_domain: dev.l-it.io
        # plus install_upi_* vars
```

```yaml
- name: Install OCP via agent-based flow
  hosts: localhost
  connection: local
  gather_facts: false
  roles:
    - role: lit.ocp.install
      vars:
        install_method: agent
        install_cluster_name: demo-ocp
        install_base_domain: dev.l-it.io
        # plus install_agent_* vars
```
