# ocp_install_upi

UPI-specific implementation for installing OpenShift (currently not implemented). The facade role `lit.ocp.ocp_install` will route here when `ocp_install_method: upi`.

## Status

UPI support is not yet available. The role currently fails fast with a clear message. Agent-based installs are available via `ocp_install_method: agent`.

## Variables

- `ocp_install_upi_platform`: target platform (e.g., vsphere) — placeholder.
- `ocp_install_upi_terraform_root`: path to Terraform root — placeholder.
- `ocp_install_upi_ignition_outdir`: path for ignition artifacts — placeholder.

## Example (will fail until implemented)

```yaml
- hosts: localhost
  connection: local
  gather_facts: false
  roles:
    - role: lit.ocp.ocp_install
      vars:
        ocp_install_method: upi
        ocp_install_cluster_name: demo-ocp
        ocp_install_base_domain: dev.l-it.io
```
