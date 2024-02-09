# Ansible role -  mto79 .system.logrotate

This is an Ansible role to install and configure logrotate.

## Table of Contents

- [Ansible role -  mto79 .system.logrotate](#ansible-role--- mto79 systemlogrotate)
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
| `system_logrotate_setup_frequency` | String |`weekly` | How often to rotate logs, can also be: `daily` or `monthly` |
| `system_logrotate_setup_keep` | String |`4` | How many files to keep |
| `system_logrotate_setup_compress` | String | `yes` | Should rotated logs be compressed or not |
| `system_logrotate_setup_dateext` | String | `no` | Should rotated logs have a filename containing the date |
| `system_logrotate_setup_packages` | String | `logrotate` | The software package to install |
| `system_logrotate_setup_config_directory` | String | `/etc` | The base directory for the configuration file(s) of logrotate |
| `system_logrotate_setup_config_file` | String | `/etc/logrotate.conf` | The main logrotate configuration file |
| `system_logrotate_setup_confd_directory` | String | `/etc/logrotate.d/` | The directory for additional (application-specific) logrotate configuration |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.logrotate"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'logrotate']
```
