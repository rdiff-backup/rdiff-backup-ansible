rdiff\_backup\_develop
====================

Install in one simple step the full development environment for rdiff-backup

Requirements
------------

n/a

Role Variables
--------------

* where to create the development environment for rdiff-backup

    rdb_develop_base_dir: "~/Workspace"

* where to install the virtualenv for developing relatively to the Git repo (an absolute path works as well)

    rdb_develop_venv: "dist/rdb"

Dependencies
------------

n/a

Example Playbook
----------------

Call for example with:

    ansible-playbook -i localhost, -c local \
      rdiffbackup.rdiff_backup.rdiff_backup_develop -K

(sudo rights are required to install packages)

    - name: Prepare a workstation for rdiff-backup development
      hosts: all
      gather_facts: false

      roles:
        - rdiff_backup_develop

License
-------

GPLv2 or later

Author Information
------------------

Eric Lavarde, maintainer of rdiff-backup
