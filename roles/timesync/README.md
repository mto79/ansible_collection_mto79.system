# [System_timesync](#system-timesync)

Install and configure timesync and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.10.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - { role: mto79.system.timesync, tags: ['system', 'timesync', 'system'] }
```

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_timesync_ntp_servers` | | |
| `system_timesync_ptp_domains` | | |
| `system_timesync_dhcp_ntp_server` | `False`| |
| `system_timesync_step_threshold` | `-1.0` | |
| `system_timesync_min_sources` | | |
| `system_timesync_ntp_hwts_interfaces` | | |
| `system_timesync_ntp_provider` | | |
| `system_timesync_max_distance` | | |

## [Maintainers](#maintainers)

Marc Ouwerkerk (<https://github.com/mto79>)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)

Apache-2.0
