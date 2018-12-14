# Debian repmgr sample config
Sample config file and sudoers file for 2ndQuadrant repmgr 4.2, and  Postgresql 11

Repmgr needs some special config on Debian, the default values usually does not work:
* systemctl manages postgresql serivce, the standard pg_ctl will not update systemctl
* there is  no pg_ctl on the path (although it can be founded under /usr/lib/postgresql/11/bin)

This is not a complete howto, but there is a great document at: https://repmgr.org/docs/4.2/quickstart.html

This example uses postgres user for replication management, however it could work with any other user too, just set the username in sudoers.con

# Usage

* Install Repmgr from postgres repo
* on each host:
** setup ssh passwordless connectivity for postgresql
** edit & Copy repmgr.conf  to /etc ( search  node_id, for <Your_node_name>, <IP or hostname of this node>)
** add the content of sudoers to /etc/sudoers
 



