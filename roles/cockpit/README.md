# Ansible role - mto79.system.cockpit

This is an Ansible role to install and configure cockpit.
Include more information about cockpit in this section.

## Table of Contents

- [Ansible role - mto79.system.cockpit](#ansible-role---mto79systemcockpit)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
    - [Setup](#setup)
    - [Upstream](#upstream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.12.0.
- The minimum version of Jinja template 2.11.3

## [Role variables](#role-variables)

### Setup

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
| `system_cockpit_upstream_packages` | String | `default` | Packages to install Cocokpit and it plugins.
| `system_cockpit_upstream_enabled` | Boolean | `true` | Flag to enable or disable cockpit.
| `system_cockpit_upstream_started` | Boolean | `true` | Flag to start or stop cockpit.
| `system_cockpit_upstream_port` | String | `9090` | Port user for running cockpit.
| `system_cockpit_upstream_manage_firewall` | Boolean | `false` | Firewall configuration for Cockpit.
| `system_cockpit_upstream_manage_selinux` | String | `false` | Seliunx configuration for Cockpit.
| `system_cockpit_upstream_certificates` | String | `` | Certificates to use for Cockpit.

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.system.cockpit"
          vars:
            __role_action: "setup"
          tags: ['system', 'system-cockpit']
```
