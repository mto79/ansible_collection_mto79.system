# Ansible role -  mto79.system.hostname

This is an Ansible role to configure the hostname on system.

## Table of Contents

- [Ansible role -  mto79.system.hostname](#ansible-role--- mto79systemhostname)
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
| `system_hostname_setup_hostname`             | String     | Any               | The hostname to set. By default whatever the inventory is set to. |
| `system_hostname_setup_reboot`               | Boolean    | true              | Should the machine be rebooted when the hostname is changed? |
| `system_hostname_setup_requirements`         | List       | `hostname`        | Package needed to set hostanme|

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.hostname"
          vars:
            __role_action: "setup"
          tags: ['system', 'system-hostname']
```
