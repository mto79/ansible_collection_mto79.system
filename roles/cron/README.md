# Ansible role -  mto79.system.cron

This is an Ansible role to install and configure cron.
Include more information about cron in this section.

## Table of Contents

- [Ansible role -  mto79.system.cron](#ansible-role----mto79systemcron)
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
| system_cron_setup_shell | string | /bin/bash | The shell to use for the cron jobs |
| system_cron_setup_path | string | /usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin | The path to use for the cron jobs |
| system_cron_setup_mailto  | string | root | The mailto to use for the cron jobs |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.system.cron"
          vars:
            __role_action: "setup"
          tags: ['system', 'system-cron']

```
