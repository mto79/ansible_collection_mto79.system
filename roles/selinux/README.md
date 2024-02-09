Ansible Role selinux
=========

This is an Ansible role to install and configure selinux.

Include more information about selinux in this section.

Table of Contents
-----------------
- [Ansible Role selinux](#ansible-role-selinux)
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
| `system_selinux_setup_packages` | String | `` |  Packages to install for selinux.
| `system_selinux_setup_state`  | String | `` |  State of selinux.
| `system_selinux_setup_policy`  | String | `` |  Policy of selinux.
| `system_selinux_setup_booleans` | String | `` |  Booleans of selinux.

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
| `system_selinux_upstream_state` | String | `` |  State of selinux.
| `system_selinux_upstream_policy`  | String | `` |  Policy of selinux.
| `system_selinux_upstream_booleans`  | List | `` |  Booleans of selinux.
| `system_selinux_upstream_fcontexts` | List | `` |  Fcontexts of selinux.
| `system_selinux_upstream_logins` | List | `` |  Logins of selinux.
| `system_selinux_upstream_ports` | List | `` |  Ports of selinux.
| `system_selinux_upstream_restore_dirs` | List | `` |  Restore dirs of selinux.
| `system_selinux_upstream_all_purge` | Boolean | `` |  All purge of selinux.
| `system_selinux_upstream_booleans_purge` | Boolean | `` |  Booleans purge of selinux.
| `system_selinux_upstream_fcontexts_purge` | Boolean | `` |  Fcontexts purge of selinux.
| `system_selinux_upstream_ports_purge` | Boolean | `` |  Ports purge of selinux.
| `system_selinux_upstream_logins_purge` | Boolean | `` |  Logins purge of selinux.

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.selinux"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'system-selinux']
