Ansible Role sos
=========

This is an Ansible role to make sosreport on a RHEL system.

Include more information about sos in this section.

Table of Contents
-----------------

- [Ansible Role sos](#ansible-role-sos)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.12.0.
- The minimum version of Jinja template 2.11.3

## [Role variables](#role-variables)

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
| `system_sos_remote_location` | String | `/tmp/sosreports` | Where to store the sosreport on the managed node.
| `system_sos_local_location`  | String | `/tmp/sosreports` | Where to store the sosreport on the controller.
| `system_sos_packages`        | List   | `sos`             | List of packages to install on the managed node.
| `system_sos_command`         | String | `sosreport`       | The sosreport command to run on the managed node.
| `system_sos_patterns`        | String | ``                | List of patterns to pass to the sosreport command.
| `system_sos_ticket_number`   | String | `from project`    | The ticket number to pass to the sosreport command.
| `system_sos_upload_user`     | String | `from project`    | The user to use to upload the sosreport.
| `system_sos_upload_password` | String | `from project`    | The password to use to upload the sosreport.

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.sos"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'sos', 'setup']
```
