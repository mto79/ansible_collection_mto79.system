Ansible Role users
=========

This is an Ansible role to install and configure users.

Include more information about users in this section.

Table of Contents
-----------------
- [Ansible Role users](#ansible-role-users)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
    - [Setup](#setup)
    - [Upsream](#upsream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.11.0.
- The minimum version of Jinja template 2.11.3

## [Role variables](#role-variables)
### Setup
| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
|`system_users_setup_ssh_key_directory` |  `String` | `ssh_keys` | `The location to store ssh keys for user` |
|`system_users_setup_shell` |  `String` | `/bin/bash` | `The default shell if not overwritten.` |
|`system_users_setup_cron_allow` |  `Boolean` | `True` | `Manage cron permissions via /etc/cron.allow` |
|`system_users_setup_create_home` |  `Boolean` | `True` | `Should homedirectories be created?` |

### Upsream
| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.users"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'users']
```
