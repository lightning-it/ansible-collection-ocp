Ansible role to manage openshift operator from the operator hub
================================================================

This role installs or uninstalls operators from the operator hub. For manually approved subscriptions, the install plan can be approved by Ansible.
It's also possible to install a specific operator version by using manage_operator_starting_csv.


Role Variables
--------------

With the values in defaults/main.yml Red Hat Single Sign-On Operator will be installed.

Example Playbook
----------------

```yaml
---
- name: Install rhsso
  hosts: localhost
  vars:
    manage_operator_name: rhsso-operator
    manage_operator_namespace: rhsso
    manage_operator_channel: stable
    manage_operator_source: redhat-operators
    manage_operator_source_namespace: openshift-marketplace
    manage_operator_target_namespaces: true
    manage_operator_deployment_name: rhsso-operator
    manage_operator_create_namespace: true
  roles:
    - role: lit.ocp.manage_operator
      tags:
        - rhsso
```

License
-------

This Ansible role is licensed under the MIT

Author
------

Dirk Egert <github@degert-it.de>
