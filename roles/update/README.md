# [System_update](#system-update)
:%%
Install and configure cockpit and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.11.0.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.update"
          vars:
            __role_action:
              - "setup"
              #- "upstream" # Uncomment to run upstream-specific tasks
          tags: ['system', 'update', 'setup']
```

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_update_autoremove` | `no` | remove unused dependency packages for all module states except `build-dep |
| `system_update_upgrade_command` | `dist` | apt_upgrade type which can be: dist, full, yes, or safe |
| `system_update_cache_valid_time` | `1` | update the apt cache if it's older than the cache_valid_time. Set in seconds.
| `system_update_reboot` | `yes` | Always or never reboot when packages have changed
| `system_update_packages_exclude` | `Empty list` | List of packages to exclude from update by holding.

## [Maintainers](#maintainers)

MTO79 (<https://github.com/mto79>)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)

MIT License
