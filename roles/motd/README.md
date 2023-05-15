# [System_motd](#system-motd)

Configure motd and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.11.0.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.motd"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'motd']

```

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_hostname` | `` | Hostname of system |
| `system_hostname_use` | `systemd` | hostname use for system |

## [Maintainers](#maintainers)

Marc Ouwerkerk (<https://github.com/mto79>)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)

MIT License
