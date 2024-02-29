# Ansible role -  mto79.system.rhc

This is an Ansible role to install and configure rhc.
Include more information about rhc in this section.

## Table of Contents

- [Ansible role -  mto79.system.rhc](#ansible-role----mto79systemrhc)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
    - [Setup](#setup)
    - [Upstream](#upstream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.11.0.
- The minimum version of Jinja template 2.11.3

## [Role variables](#role-variables)

### Setup

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
|`system_rhc_upstream_auth` |  | | |
|`system_rhc_upstream_baseurl`  | | | |
|`system_rhc_upstream_environments` | | | |
|`system_rhc_upstream_insights` | | | |
|`system_rhc_upstream_organization` | | | |
|`system_rhc_upstream_services` | | | |
|`system_rhc_upstream_release` | | | |
|`system_rhc_upstream_repositories` | | | |
|`system_rhc_upstream_server` | | | |
|`system_rhc_upstream_state` | | | |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.system.rhc"
          vars:
            __role_action: "setup"
          tags: ['system', 'rhc']
```
