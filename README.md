## Ansible role to provision some versions of Request Tracker

Request Tracker:

https://bestpractical.com/

https://github.com/bestpractical/rt

Dependencies:

Ansible role deimos.mariadb

RT depends on a PostGres or MySQL database. Right now, this role depends on MariaDB, which is apparently a non-Oracle fork of MySQL. It seems to work OK so far. 
