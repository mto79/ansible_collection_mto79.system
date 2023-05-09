# [System_cockpit](#system-cockpit)
:%%
Install and configure cockpit and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.10.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.cockpit"
          vars:
            __role_action:
              - "setup"
              #- "vendor" # Uncomment to run vendor-specific tasks
          tags: ['system', 'cockpit', 'setup']
```

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_cockpit_` | | |

## [Maintainers](#maintainers)

Marc Ouwerkerk (<https://github.com/mto79>)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)

MIT License
