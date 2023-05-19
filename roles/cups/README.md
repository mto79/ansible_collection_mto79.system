# [System_cups](#system-cups)

Install and configure cups and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.10.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.cups"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'firewall']
```

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_cups_` | | |

## [Maintainers](#maintainers)

MTO79 (<https://github.com/mto79>)

## [Todo](#todo)

## [License](#license)

MIT License
