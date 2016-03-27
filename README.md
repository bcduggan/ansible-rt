Ansible role for Request Tracker
================================

This Ansible role installs Best Practical's Request Tracker (RT). It optionally installs certain RT extensions.

https://bestpractical.com/
https://github.com/bestpractical/rt

Requirements
------------

RT depends on many Perl modules, Apache with either mod_perl or mod_fcgid, and PostgreSQL or MySQL.

RT prefers mod_fcgid and MySQL.

This role uses MariaDB instead of MySQL.

Role Variables
--------------

Check defaults/main.yml.

Use rt_version to select the RT version to install.


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: bcduggan.rt, rt_version: 4.2.12 }

License
-------

GPLv3


Author Information
------------------

Brian Duggan
