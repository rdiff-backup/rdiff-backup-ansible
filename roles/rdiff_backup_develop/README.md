rdiff\_backup\_develop
====================

Install in one simple step the full development environment for rdiff-backup

Requirements
------------

You'll need to make sure that your (GitHub) SSH key is loaded with ssh-agent/ssh-add prior to calling this role so that you can clone the Git repos.

The role is mostly idempotent.
It doesn't clone already cloned Git repos, but it fails if there are uncommitted changes.

Role Variables
--------------

* where to create the development environment for rdiff-backup

    rdb_develop_base_dir: "~/Workspace"

* where to install the virtualenv for developing relatively to the Git repo (an absolute path works as well)

    rdb_develop_venv: "dist/rdb"

Dependencies
------------

You will need the collection 'community.general' for its module 'pacman' if you want to use this collection under ArchLinux and derivatives (e.g. Manjaro).

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

MIT

Author Information
------------------

Eric Lavarde, maintainer of rdiff-backup
