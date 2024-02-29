# Ansible role -  mto79.system.timezone

This is an Ansible role to configure timezone.

## Table of Contents

- [Ansible role -  mto79.system.timezone](#ansible-role----mto79systemtimezone)
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
| `system_timezone_setup_timezone` | String | `` |  Given timezone for system. |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.system.timezone"
          vars:
            __role_action: "setup"
          tags: ['system', 'system-timezone']
```
