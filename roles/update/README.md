# Ansible role -  mto79.system.update

This is an Ansible role to update your system.

## Table of Contents

- [Ansible role -  mto79 .system.timesync](#ansible-role--- mto79 systemtimesync)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role Variables](#role-variables)
    - [Setup](#setup)
    - [Upstream](#upstream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.10.
- The minimum version of Jinja template 2.11.3

## [Role Variables](#role-variables)

### Setup

| Variable                                     | Type       | Default           | Description |
|----------------------------------------------|------------|-------------------|-------------|

### Upstream

| Variable | Default | Description |
| -------- | ------- | ----------- |

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.system.update"
          vars:
            __role_action: "setup"
          tags: ['system', 'system-update']
```
