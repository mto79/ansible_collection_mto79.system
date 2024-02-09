# Ansible role -  mto79 .system.network

This is an Ansible role to install and configure network.

## Table of Contents

- [Ansible role -  mto79 .system.network](#ansible-role--- mto79 systemnetwork)
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

| Variable                                     | Type       | Default           | Description |
|----------------------------------------------|------------|-------------------|-------------|
| ``           | String     |                |  |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |


## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.network"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'system-network']
```
