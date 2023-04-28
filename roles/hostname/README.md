# [System_hostname](#system-hostname)

Install and configure hostname and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.10.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.hostname"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'hostname', 'setup']

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
Apache-2.0
