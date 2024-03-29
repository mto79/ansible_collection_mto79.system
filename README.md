# [ansible_collection_mto79.system](#ansible_collection_mto79system)

MTO79 - Ansible Collection - System

## [Description](#description)

Ansible collection that provisions linux systems.

## Included content

<!--start collection content-->
### Lookup plugins

Name | Description
--- | ---

### Modules

Name | Description | Tests
--- | --- | ---

### Roles

Name | Description | Tests
--- | --- | ---
[mto79.system.bootstrap](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/bootstrap/README.md)| Bootstrap your system. | Make system ready for ansible.
[mto79.system.cups](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/cups/README.md)| Configure EPEL on your system. | RedHat based distros only.
[mto79.system.dnf](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/dnf/README.md)| Configure DNF on your system. | RedHat based distros only.
[mto79.system.epel](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/epel/README.md)| Configure EPEL on your system. | RedHat based distros only.
[mto79.system.hostname](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/hostname/README.md)| Configure hostname on system.| Tests currently unavailable.
[mto79.system.hosts](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/hosts/README.md)| Configure host file on your system.| Tests currently unavailable.
[mto79.system.issue](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/issue/README.md)| Configure /etc/issue on system.| Tests currently unavailable.
[mto79.system.motd](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/motd/README.md)| Configure MOTD on system.| Tests currently unavailable.
[mto79.system.rhc](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/rhc/README.md)| Remote Host configuratio (RedHat).| Tests currently unavailable.
[mto79.system.selinux](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/selinux/README.md)| Install and configure SELinux.| Tests currently unavailable.
[mto79.system.timesync](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/timesync/README.md)| Install and configure Timesync.| Tests currently unavailable.
[mto79.system.timezone](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/timezone/README.md)| Install and configure Timezone.| Tests currently unavailable.
[mto79.system.update](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/update/README.md)| Update your system.| Tests currently unavailable.
[mto79.system.users](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/users/README.md)| Install and configure Users.| Tests currently unavailable.
<!--end collection content-->

## [Installing this collection](#installing-this-collection)

### Local installation

You can install the MTO79 System collection locally, if you acquired a tarball from the [releases page](https://github.com/mto79/ansible_collection_mto79.system/releases) as follows:

    ansible-galaxy collection install /path/to/mto79-system-X.Y.Z.tar.gz

You can also include it in a `requirements.yml` file and install it with
`ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - source: /path/to/mto79-system-X.Y.Z.tar.gz
    type: file
```

### From the Galaxy

You can install the System collection with the Ansible Galaxy CLI:

    ansible-galaxy collection install mto79.system

You can also include it in a `requirements.yml` file and install it with
`ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - name: mto79.system
    version: X.Y.Z
```

## [Requirements](#requirements)

Make sure you have the following requirements installed on your control node.

```yaml
- name: fedora.linux_system_roles
  version: 1.36.3
  source: https://galaxy.ansible.com
```

## [Pre-commit](#pre-commit)

Install pre-commit

```bash
pip install pre-commit
```

Set hooks in .pre-commit-config.yaml

```bash
repos:
- repo: https://github.com/ansible/ansible-lint.git
  rev: v4.2.0
  hooks:
    - id: ansible-lint
      files: \.(yaml|yml)$
```

Enable pre-commit for your git repository

```bash
$ pre-commit install
pre-commit installed at .git/hooks/pre-commit
```

Testing pre-commit

```bash
pre-commit run --all-files
Ansible-lint.............................................................Passed
```

or just type:

```bash
git commit
```

## [More information](#more-information)

* [MTO Website](https://mto.nu)

## [Licensing](#licensing)

See [LICENSE](LICENSE).
