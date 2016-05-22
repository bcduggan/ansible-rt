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

This role assumes CentOS 7.2 with SELinux enabled or disabled.

Role Variables
--------------

Check defaults/main.yml.

Use rt_version to select the RT version to install. See vars/rt_versions.yml for supported versions.
Use selinux to enable or disable selinux labels.
Use cpanm_notest to enable or disable running tests after building Perl modules.
Use perlbrew_notest to enable or disable running tests after building the desired Perl version.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: bcduggan.rt
	   rt_version: rt-4.2.12
	   selinux: true
	   cpanm_notest: false
	   perlbrew_notest: false

License
-------

GPLv3


Author Information
------------------

Brian Duggan
