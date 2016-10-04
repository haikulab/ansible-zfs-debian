ansible-zfs-debian for Debian 8 Jessie
============

Ansible role for initial server provisioning by doing some super basic actions such as updating the system and installing core packages.

## Overwriting Variables

The `vars/main.yml` file should contain your list of packages you want to install in order to override defaults found in `defaults/main.yml`. Additionally, you can overwrite the variables as part of your playbook.

```yml
---
zfs_repo_url: "http://archive.zfsonlinux.org/debian/pool/main/z/zfsonlinux/zfsonlinux_6_all.deb" 
zfs_packages:
  - linux-image-amd64
  - debian-zfs
```

__Note: Some packages will already be in place with default Ubuntu install but there is no harm in making sure.__

## Debugging

If you run into errors, uncomment the `- debug: msg="{{ ... }}"` statements.
