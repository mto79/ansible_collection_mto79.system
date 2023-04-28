# [System_timezone](#system-timezone)

Install and configure timezone and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.10.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.timezone"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'timezone', 'setup']

```

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_timezone` | `Europe/Amsterdam` | Standard timezone|
| `system_hwclock` | `UTC` | Default system time (only linux) |

## [Maintainers](#maintainers)

Marc Ouwerkerk (<https://github.com/mto79>)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)
Apache-2.0
