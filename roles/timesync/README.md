# Ansible role -  mto79.system.timesync

This is an Ansible role to install and configure timesync.
Include more information about timesync in this section.

## Table of Contents

- [Ansible role -  mto79 .system.timesync](#ansible-role--- mto79 systemtimesync)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role Variables](#role-variables)
    - [Setup](#setup)
    - [Upstream](#upstream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.10.
- The minimum version of Jinja template 2.11.3

## [Role Variables](#role-variables)

### Setup

| Variable                                     | Type       | Default           | Description |
|----------------------------------------------|------------|-------------------|-------------|

### Upstream

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_timesync_upstream_ntp_servers` | | |
| `system_timesync_upstream_ptp_domains` | | |
| `system_timesync_upstream_dhcp_ntp_server` | `False`| |
| `system_timesync_upstream_step_threshold` | `-1.0` | |
| `system_timesync_upstream_min_sources` | | |
| `system_timesync_upstream_ntp_hwts_interfaces` | | |
| `system_timesync_upstream_ntp_provider` | | |
| `system_timesync_upstream_max_distance` | | |

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.timesync"
          vars:
            __role_action: "setup"
          tags: ['system', 'system-timesync']
```
