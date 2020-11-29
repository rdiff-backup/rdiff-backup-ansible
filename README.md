rdiff_backup
============

A role to install rdiff-backup on different platforms.

Requirements
------------

None.

Role Variables
--------------

The variables are defined in the [defaults/main.yml](defaults/main.yml) file.

Dependencies
------------

None.

Example Playbook
----------------

The role can be used by default without any variable:

    - hosts: servers
      roles:
         - { role: rdiffbackup.rdiff_backup }

Make sure ansible-playbook can become root to install software, e.g.
using the `-K` option.

License
-------

MIT

Author Information
------------------

Go to https://github.com/rdiff-backup/rdiff-backup-ansible to report issues
or support the development of this role.
Go to https://rdiff-backup.net/ for any other question.
