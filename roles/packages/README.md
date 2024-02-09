# Ansible role -  mto79 .system.packages

This is an Ansible role to install and configure packages.

Include more information about packages in this section.

## Table of Contents

- [Ansible role -  mto79 .system.packages](#ansible-role--- mto79 systempackages)
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
|`system_packages_setup_conflicting_items` | `List` | `[]` | List of conflicting packages to delete |
|`system_packages_setup_items` | `List` | `[]` | List of packages to install |
|`system_packages_setup_pip_items` | `List` | `[]` | List of PIP packages |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.packages"
          vars:
            __role_action:
              - "setup"
          tags: ["system", "system-packages"]
```
