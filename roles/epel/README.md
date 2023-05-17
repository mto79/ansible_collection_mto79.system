# [System_epel](#system-epel)

Install and configure EPEL and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.11.0.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.epel"
          vars:
            __role_action:
              - "setup"
              #- "upstream" # Uncomment to run upstrea-specific tasks
          tags: ['system', 'epel']
```

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_epel_gpg_key` | | GPG Key for EPEL repo |
| `system_epel_url` | | URL EPEL release |
| `system_epel_next_url` | | URL EPEL NEXT Release |

## [Maintainers](#maintainers)

MTO79 (<https://github.com/mto79>)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)

MIT License
