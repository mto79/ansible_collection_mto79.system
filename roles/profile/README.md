# Ansible role - mto79.system.profile

This is an Ansible role to install and configure profile.
Include more information about profile in this section.

## Table of Contents

- [Ansible role - mto79.system.profile](#ansible-role---mto79systemprofile)
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

## [Example Playbook](#example-playbook)

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.system.firewall"
          vars:
            __role_action: "setup"
          tags: ['system', 'system-firewall']

```
