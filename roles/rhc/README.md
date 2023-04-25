# [Hetzner-Server](#hetzner-server)

Hetzner role to provisioning a dedicated server with server

## [Requirements](#requirements)

* The minimum version of Ansible required is 2.10.
* The minimum version of Jinja template 2.11.3

## [Example Playbook](#example-playbook)

```yaml
---
- name: playbook
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - { role: mto79.hetzner.server, tags: ['mto79', 'hetzner-server', 'system'] }

  collections:
    - mto79.hetzner.server

```

## [Role variables](#role-variables)

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `hetzner_server_api_url` | `https://robot-ws.your-server.de` | Username for Hetzner Dedicated server |
| `hetzner_server_api_username` | `Empty` | Username for Hetzner Dedicated server |
| `hetzner_server_api_password` | `Empty` | Password for Hetzner Dedicated server |
| `hetzner_server_hostname` | `Empty` | Hostname for Hetzner Dedicated server |
| `hetzner_server_ip` | `xxx.xxx.xxx.xxx` | IP address for Hetzner Dedicated server |
| `hetzner_server_disk1` | `sda` | Disk1 for Hetzner Dedicated server |
| `hetzner_server_disk2` | `sdb` | Disk2 for Hetzner Dedicated server |
| `hetzner_server_image` | `/root/.oldroot/nfs/install/../images/CentOS-80-stream-amd64-base.tar.gz` | Default image for Hetzner Dedicated server |
| `hetzner_server_image_ignore_errors` | `False` | To overlook errors image for Hetzner Dedicated server |

## [Standards](#standards)

## [Maintainers](#maintainers)

Marc Ouwerkerk (https://github.com/mto79)

## [Todo](#todo)

* testing

## [License](#license)

Apache-2.0
