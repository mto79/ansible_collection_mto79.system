# [System-users](#system-users)

Configure users and groups on your system.

# [Role Variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `core_users_ssh_key_directory` | `ssh_keys` | Directory where ssh_key is placed |
| `core_users_shell` | `/bin/bash` | Users shell |
| `core_users_cron_allow` | `yes` | Can User create cron jobs? |
| `core_users_create_home` | `yes` | Create users home directory |
| `core_users_requirements` |
| `core_users_group_list` |  | name: group_name gid: group_id |
| `core_users_user_list`  |  | name: user_name comment: user_full_name uid: user_id group: group_name home: users_home_dir cron_allow: yes / no |

## [Maintainers](#maintainers)

Marc Ouwerkerk (<https://github.com/mto79>)

## [Todo](#todo)

* Standaardwaarden voor molecule testen toevoegen

## [License](#license)

Apache-2.0
