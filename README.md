## Ansible role to provision some versions of Request Tracker

To use:

> $ cd ansible-rt
> $ ansible-galaxy install -r requirements.txt -p roles
> $ vagrant up rt

The provisioning process will take several minutes the first time. Both Vagrant and Ansible will need to download a lot of stuff. Make sure you have a solid Internet connection, then grab some coffee, tea, hot or cold water, a cigarette, etc.

Request Tracker:

https://bestpractical.com/

https://github.com/bestpractical/rt

Dependencies:

Ansible role deimos.mariadb

RT depends on a PostGres or MySQL database. Right now, this role depends on MariaDB, which is apparently a non-Oracle fork of MySQL. It seems to work OK so far. 
