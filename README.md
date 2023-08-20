# Ansible Collection - rdiffbackup.rdiff\_backup

The present collection will sample Ansible automation artefacts of interest for the
community.

## Install rdiff-backup

We'll start with a [role to install rdiff-backup](roles/rdiff_backup_install/README.md)
on multiple platforms.

Once you have ansible installed, you can simply install this collection with:

```
ansible-galaxy collection install [-f] rdiffbackup.rdiff_backup
```

> **NOTE:** the `-f` is required if you have already installed and want to get the latest version

The following playbook is then sufficient to install rdiff-backup:


```
- name: install rdiff-backup on Linux and Windows
  hosts: all

  roles:
  - rdiffbackup.rdiff_backup.rdiff_backup_install
```

Depending on your exact setup, the following command can be then sufficient, as the role comes with all necessary meaningful defaults:

```
ansible-playbook -i myhost, install-rdiff-backup.yml [-k] [-K]
```

> **NOTE:** use `-k` to enter a login password, `-K` to enter a become password (on Linux, to become root).

## Develop rdiff-backup

A simple role and playbook do exist to install all dependencies necessary to develop rdiff-backup, e.g. with:

    ansible-playbook -i localhost, -c local \
      rdiffbackup.rdiff_backup.rdiff_backup_develop -K

This playbook is only developed and tested for Fedora, but you are welcome to offer your help for other platforms.

## CHANGELOG

* v1.2.0 / 2023-08-20 - add `rdiff_backup_develop` role and playbook
* v1.1.1 / 2020-12-18 - fix typo in role metadata
* v1.1.0 / 2020-12-17 - add support for Debian, Ubuntu and Windows.
* v1.0.0 / 2020-12-11 - initial release with CentOS/RHEL and Fedora support.
