Ansible Role pam_limits
=========

This is an Ansible role to install and configure pam_limits.

Include more information about pam_limits in this section.

Table of Contents
-----------------
- [Ansible Role pam\_limits](#ansible-role-pam_limits)
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
| `system_pam_limits_setup_items` | List | `` |  List of PAM limits.

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.pam_limits"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'pam_limits']
