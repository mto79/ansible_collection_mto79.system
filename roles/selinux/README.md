# [System-selinux](#system-selinux)

Install and configure Selinux and its required libraries on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.10.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: servers
      roles:
        - { role: mto79.system.selinux, tags: ['system', 'selinux', 'system'] }
```

## [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `system_selinux_state`| `enforcing` | State of SELinux |
| `system_selinux_policy` | `targeted` | Policy of SELinux |
| `system_selinux_reboot` | `yes` | Machine reboot after SELinux changes |
| `system_selinux_booleans`| `default settings per distro` | Enable (or disable) booleans |

The policy differs per distribution, mostly because Debian and Ubuntu use 'default' and other distributions use 'targeted'.

See for usage variable system_selinux_booleans the defaults.yml

## [Maintainers](#maintainers)

Marc Ouwerkerk (https://github.com/mto79)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)

Apache-2.0
