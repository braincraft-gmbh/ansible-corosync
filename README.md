Role Name
=========

This role deploys corosync with basic setup and resources for an HA pair.

Requirements
------------

This role requires two hosts able to communicate with each other via an internal
network and two available networks providing floating IPs.

Role Variables
--------------

```
clustername: cluster
ip_int: 192.168.0.1
floating_ip_ext: 1.2.3.4
floating_ip_int: 192.168.0.100
ha_host_active: host1
ha_host_active_ip_int: 192.168.0.1
ha_host_standby: host2
ha_host_standby_ip_int: 192.168.0.2
```


Dependencies
------------

This role currently uses `lsyncd` as one of the resources (to synchronize
folders) between two hosts. As such, `lsyncd` should be present in the system.

Example Playbook
----------------

    - hosts: ha
      roles:
         - bc.corosync

License
-------

GNU GPLv3

Author Information
------------------

Gualter Barbas Baptista <gualter@ecobytes.net>
