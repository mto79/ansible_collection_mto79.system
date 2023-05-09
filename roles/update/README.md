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
| `system_update_` | | |

## [Maintainers](#maintainers)

MTO79 (<https://github.com/mto79>)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)

MIT License
