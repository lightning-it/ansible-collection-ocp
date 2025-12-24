# ocp_install_agent

Agent-based installer for OpenShift Container Platform. Prepares configuration artifacts, manages ignition files, powers on infrastructure, and persists generated secrets (e.g., kubeconfig) in Vault.

## Usage

```yaml
- hosts: localhost
  gather_facts: false
  roles:
    - role: lit.ocp.ocp_install_agent
      vars:
        ocp_install_cluster_name: demo
        ocp_install_base_domain: corp.example.com
        ocp_install_delegate_to: localhost
        ocp_install_machine_network: 10.10.0.0/23
        ocp_install_vsphere: true
        ocp_install_vcenter_hostname: vcsa.corp.example.com
        ocp_install_vcenter_username: administrator@vsphere.local
        ocp_install_vcenter_password: "{{ lookup('env','VSPHERE_PASSWORD') }}"
        ocp_install_pullsecret_lookup: secret=platform/data/demo/install:pullsecret
```

## Variables

- `ocp_install_*`: core installation inputs covering cluster identity (`ocp_install_cluster_name`, `ocp_install_base_domain`, `ocp_install_version`), topology/networking (`ocp_install_machine_network`, `ocp_install_gateway`, `ocp_install_dns_servers`, `ocp_install_ifname`), and image/pull secret data.
- vSphere-specific variables (`ocp_install_vsphere`, `ocp_install_vcenter_*`, `ocp_install_vsphere_datacenter`, `ocp_install_vsphere_network`, etc.) drive VM provisioning when targeting VMware.
- Vault integration relies on `ocp_install_hashi_vault_auth_method`, `ocp_install_engine_mount_point`, and lookup strings (`ocp_install_pullsecret_lookup`, `g_root_ca_lookup`, etc.).
- Tags such as `ocp_install_post` and `ocp_install_infra` let you rerun post-install steps or infra/app-node configuration independently.
