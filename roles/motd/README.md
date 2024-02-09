Ansible Role motd
=========

This is an Ansible role to install and configure motd.

Include more information about motd in this section.

Table of Contents
-----------------
- [Ansible Role motd](#ansible-role-motd)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.12.0.
- The minimum version of Jinja template 2.11.3

## [Role variables](#role-variables)

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
| `system_motd_setup_msg` | String | `` | Optional message of the day.
| `system_motd_setup_update_scripts`  | String | `` | List of motd pre-set script with Ubuntu.

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.motd"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'motd']

```
