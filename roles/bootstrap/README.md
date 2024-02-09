# Ansible role -  mto79 .system.bootstrap

This is an Ansible role to install and configure bootstrap.
Include more information about bootstrap in this section.

Table of Contents
-----------------

- [Ansible role -  mto79 .system.bootstrap](#ansible-role--- mto79 systembootstrap)
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
| `system_bootstrap_setup_wait_for_host` | Boolean | `False` | Do you want to wait for the host to be available?
| `system_bootstrap_setup_timeout`  | Number | `3` | The number of seconds you want to wait during connection test before failing..
| `system_bootstrap_setup_become` | Boolean   | `True` | Tell the role to "become" or not..

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.bootstrap"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'bootstrap']

```
