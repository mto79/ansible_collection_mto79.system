# Ansible role -  mto79.system.sysctl

This is an Ansible role to install and configure sysctl settings.

## Table of Contents

- [Ansible role -  mto79 .system.sysctl](#ansible-role--- mto79 systemsysctl)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
    - [Setup](#setup)
    - [Upstream](#upstream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

| Name             | Minimum Version |
|------------------|:---------------:|
| ansible          | 2.11.0          |
| jinja2           | 2.11.3          |

## [Role variables](#role-variables)

### Setup

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
| `system_sysctl_setup_packages` | List | `[]` | List of packages to install |
| `system_sysctl_setup_set` | Boolean | `True` | Whether to set sysctl settings |
| `system_sysctl_setup_reload` | Boolean | `True` | Whether to reload sysctl settings |
| `system_sysctl_setup_items` | List | `[]` | List of sysctl settings to set |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.system.sysctl"
          vars:
            __role_action: "setup"
          tags: ['system', 'sysctl']
```
