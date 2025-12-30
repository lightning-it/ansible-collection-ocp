# install_upi

UPI-specific implementation for installing OpenShift (currently not implemented). The facade role `lit.ocp.install` will route here when `install_method: upi`.

## Status

UPI support is not yet available. The role currently fails fast with a clear message. Agent-based installs are available via `install_method: agent`.

## Variables

- `install_upi_platform`: target platform (e.g., vsphere) — placeholder.
- `install_upi_terraform_root`: path to Terraform root — placeholder.
- `install_upi_ignition_outdir`: path for ignition artifacts — placeholder.

## Example (will fail until implemented)

```yaml
- hosts: localhost
  connection: local
  gather_facts: false
  roles:
    - role: lit.ocp.install
      vars:
        install_method: upi
        install_cluster_name: demo-ocp
        install_base_domain: dev.l-it.io
```
