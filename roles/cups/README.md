Ansible Role cups
=========

This is an Ansible role to install and configure cups.

Include more information about cups in this section.

Table of Contents
-----------------

- [Ansible Role cups](#ansible-role-cups)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role Variables](#role-variables)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.10.
- The minimum version of Jinja template 2.11.3

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_cups_` | | |

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.cups"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'firewall']
```
