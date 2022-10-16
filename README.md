# ansible_collection_mto79.system

MTO79 - Ansible Collection - System

## Description

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
[mto79.system.selinux](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/selinux/README.md)| Install and configure SELinux.| Tests currently unavailable.
[mto79.system.timesync](https://github.com/mto79/ansible_collection_mto79.system/blob/main/roles/timesync/README.md)| Install and configure SELinux.| Tests currently unavailable.
<!--end collection content-->

## Installing this collection

### Locally

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

You can install the Checkmk collection with the Ansible Galaxy CLI:

    ansible-galaxy collection install mto79.system

You can also include it in a `requirements.yml` file and install it with
`ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - name: mto79.system
    version: X.Y.Z
```

## More information

* [MTO Website](https://mto.nu)

## Licensing

See [LICENSE](LICENSE).
