# Ansible role -  mto79 .system.sshd

This is an Ansible role to install and configure SSH client.

## Table of Contents

- [Ansible role -  mto79 .system.sshd](#ansible-role--- mto79 systemsshd)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
    - [Setup](#setup)
    - [Upstream](#upstream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

| Name             | Minimum Version |
|------------------|:---------------:|
| ansible          | 2.11.0          |
| jinja2           | 2.11.3          |

## [Role variables](#role-variables)

### Setup

| Variable                                     | Type       | Default           | Description |
|----------------------------------------------|------------|-------------------|-------------|
| `system_sshd_setup_address_family`           | String     | Any               | Specifies the protocol family (IPv4, IPv6) to be used. |
| `system_sshd_setup_listen_addresses`         | List       | ["0.0.0.0", "::"] | Addresses on which the SSH server listens. |
| `system_sshd_setup_host_keys`                | List       | [Paths to keys]   | Specifies the host keys for the SSH server. |
| `system_sshd_setup_rekey_limit`              | String     | "default none"    | The limit after which the session key is re-exchanged. |
| `system_sshd_setup_syslog_facility`          | String     | "AUTH"            | The syslog facility that the server will use for logging. |
| `system_sshd_setup_loglevel`                 | String     | "INFO"            | The verbosity level for logging. |
| `system_sshd_setup_login_grace_time`         | String     | "2m"              | Time allowed for successful login. |
| `system_sshd_setup_permit_root_login`        | String     | "yes"             | Whether root can log in using SSH. |
| `system_sshd_setup_strict_modes`             | String     | "yes"             | Checks file modes and ownership of user's files. |
| `system_sshd_setup_max_auth_tries`           | String     | "6"               | Maximum number of authentication attempts. |
| `system_sshd_setup_max_sessions`             | String     | "10"              | Maximum number of open sessions per network connection. |
| `system_sshd_setup_pub_key_authentication`   | String     | "yes"             | Enables public key authentication. |
| `system_sshd_setup_authorized_key_file`      | String     | ".ssh/authorized_keys" | Location of the authorized_keys file. |
| `system_sshd_setup_authorized_prinicpals_file` | String  | "none"            | Specifies the file that lists principal names. |
| `system_sshd_setup_authorized_keys_command`  | String     | "none"            | Command to fetch public keys. |
| `system_sshd_setup_authorized_keys_command_user` | String | "nobody"         | User under which the authorized_keys_command is run. |
| `system_sshd_setup_host_based_authentication` | String   | "no"              | Enables host-based authentication. |
| `system_sshd_setup_ignore_user_known_hosts`  | String     | "no"              | Ignore the user's `~/.ssh/known_hosts`. |
| `system_sshd_setup_ignore_rhosts`            | String     | "yes"             | Ignore `rhosts` and `shosts` files. |
| `system_sshd_setup_permit_empty_passwords`   | String     | "no"              | Allows login to accounts with empty passwords. |
| `system_sshd_setup_password_authentication`  | String     | "yes"             | Enables password authentication. |
| `system_sshd_setup_challenge_response_authentication` | String | "no"         | Enables challenge-response authentication. |
| `system_sshd_setup_gssapi_authentication`    | String     | "yes"             | Enables GSSAPI (Kerberos) authentication. |
| `system_sshd_setup_gssapi_cleanup_credentials` | String  | "no"              | Whether to automatically destroy user credentials on logout. |
| `system_sshd_setup_gssapi_strict_acceptor_check` | String | "yes"            | Check the acceptor's name in GSSAPI. |
| `system_sshd_setup_gssapi_key_exchange`      | String     | "no"              | Enables GSSAPI-based key exchange. |
| `system_sshd_setup_gssaip_enable_k5_users`   | String     | "no"              | Allow Kerberos V5 authentication. |
| `system_sshd_setup_use_pam`                  | String     | "yes"             | Enables or disables PAM authentication. |
| `system_sshd_setup_allow_agent_forwarding`   | String     | "yes"             | Allows forwarding of the SSH authentication agent. |
| `system_sshd_setup_allow_tcp_forwarding`     | String     | "yes"             | Allows TCP forwarding (useful for tunnels). |
| `system_sshd_setup_gateway_ports`            | String     | "no"              | Allows remote hosts to connect to local forwarded ports. |
| `system_sshd_setup_x11_forwarding`           | String     | "yes"             | Enables X11 forwarding. |
| `system_sshd_setup_x11_display_offset`       | String     | "10"              | Display number offset for X11 forwarding. |
| `system_sshd_setup_x11_use_localhost`        | String     | "yes"             | Use localhost for X11 forwarding. |
| `system_sshd_setup_permit_tty`               | String     | "yes"             | Allow TTY allocation. |
| `system_sshd_setup_print_motd`               | String     | "no"              | Print the MOTD upon login. |
| `system_sshd_setup_print_last_log`           | String     | "yes"             | Show last login information. |
| `system_sshd_setup_tcp_keep_alive`           | String     | "yes"             | Send keepalive messages over the network. |
| `system_sshd_setup_permit_user_environment`  | String     | "no"              | Allow users to set environment options. |
| `system_sshd_setup_compression`              | String     | "delayed"         | Specifies when to compress data. |
| `system_sshd_setup_client_alive_interval`    | String     | "30"              | Interval in seconds for sending keepalive messages. |
| `system_sshd_setup_client_alive_count_max`   | String     | "3"               | Maximum number of keepalive messages before disconnecting. |
| `system_sshd_setup_show_patch_level`         | String     | "no"              | Show the patch level of the SSH server. |
| `system_sshd_setup_use_dns`                  | String     | "no"              | Enable DNS checking during authentication. |
| `system_sshd_setup_pid_file`                 | String     | "/var/run/sshd.pid" | Location of the PID file for the SSHD process. |
| `system_sshd_setup_max_startups`             | String     | "10:30:100"       | Specifies the maximum number of concurrent unauthenticated connections. |
| `system_sshd_setup_permit_tunnel`            | String     | "no"              | Allow tun(4) device forwarding. |
| `system_sshd_setup_chroot_directory`         | String     | "none"            | Directory for chrooting users after authentication. |
| `system_sshd_setup_version_addendum`         | String     | "none"            | Specifies the version string addendum. |
| `system_sshd_setup_banner`                   | String     | "none"            | Specifies the path to the SSH banner. |
| `system_sshd_setup_accept_envs`              | List       | [List of env vars] | Specifies environment variables to accept. |
| `system_sshd_setup_subsystem`                | String     | "sftp {{ system_sshd_setup_sftp_server }}" | Configures an external subsystem (e.g., SFTP). |
| `system_sshd_setup_trusted_user_ca_keys`     | String     | "none"            | Specifies trusted CA keys for user authentication. |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
| `system_sshd_upstream_user` | Object | null | Whether to change global configuration or per-user one |
| `system_sshd_upstream_skip_defaults` | String | `auto` | default OS values or start from scratch |
| `system_sshd_upstream_drop_in_name` | String | `omit` | The name to be used as part of filename in drop-in directory |
| `system_sshd_upstream_ssh` | Array | `[]` | Dict of configuration options |
| `system_sshd_upstream_additional_packages` | List | `[]` | List of additional packages to install |
| `system_sshd_upstream_config_owner` | Object | `null` | Override value for the owner configuration file |
| `system_sshd_upstream_config_group` | Object | `null` | Override values for the group and mode of configuration file |
| `system_sshd_upstream_config_mode` | Object | `null` | Override values for the mode of configuration file |
| `system_sshd_upstream_config_file` | Object | `null` | Override for the configuration file we are writing
| `system_sshd_upstream_backup` | Boolean | `True` | Whether to backup the original configuration file |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: " mto79 .system.sshd"
          vars:
            __role_action:
              - "setup"
          tags: ['system', 'system-sshd']
```
