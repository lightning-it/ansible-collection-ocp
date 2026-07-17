# install_upi

UPI-specific implementation for installing OpenShift (currently not implemented). The facade role `lit.ocp.install` will route here when `install_method: upi`.

## Requirements

None.

## Variables

- `install_upi_platform`: target platform (e.g., vsphere) - placeholder.
- `install_upi_terraform_root`: path to Terraform root - placeholder.
- `install_upi_ignition_outdir`: path for ignition artifacts - placeholder.

## Dependencies

None.

## Example Playbook

```yaml
---
- name: Use lit.ocp.install_upi
  hosts: all
  become: true
  roles:
    - role: lit.ocp.install_upi
```

## License

MIT

## Author

Lightning IT

## Additional Notes

### Status

UPI support is not yet available. The role currently fails fast with a clear message. Agent-based installs are available via `install_method: agent`.

### Example (will fail until implemented)

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
