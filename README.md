Ansible role for Request Tracker
================================

This Ansible role installs Best Practical's Request Tracker (RT). It optionally installs certain RT extensions.

https://bestpractical.com/
https://github.com/bestpractical/rt

Requirements
------------

RT depends on many Perl modules, Apache with either mod_perl or mod_fcgid, and PostgreSQL or MySQL.

RT prefers mod_fcgid and MySQL.

Most Perl modules that RT depends on are in apt (other packaging systems are untested), so this role installs those modules from apt first.

This role also configures CPAN access, which the RT installer uses to fetch any Perl dependencies that it can't install through apt.

This role uses MariaDB instead of MySQL.

Role Variables
--------------

Check defaults/main.yml.

Use rt_version to select the RT version to install. There should also be a variable containing a list of extensions to install at provision-time.


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
