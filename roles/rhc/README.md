# [System-rhc](#system-rhc)

Role for subscribing and managing RHC/Insight on your system.

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.10.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: "mto79.system.rhc"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'rhc', 'setup']
```

## [Role variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
|`system_rhc_auth` |  | |
|`system_rhc_baseurl`  | |
|`system_rhc_environments` | |
|`system_rhc_insights` | |
|`system_rhc_organization` | |
|`system_rhc_proxy` | |
|`system_rhc_release` | | |
|`system_rhc_repositories` | |
|`system_rhc_server` | |
|`system_rhc_state` | |

## [Standards](#standards)

## [Maintainers](#maintainers)

Marc Ouwerkerk (https://github.com/mto79)

## [Todo](#todo)

* testing

## [License](#license)

MIT License
