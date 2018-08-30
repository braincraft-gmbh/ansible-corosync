Role Name
=========

This role deploys corosync with basic setup and resources for an HA pair.

Requirements
------------

This role requires two hosts able to communicate with each other via an internal network and two available networks providing floating IPs.

Role Variables
--------------

clustername: cluster
ip_int: 192.168.0.1
floating_ip_ext: 1.2.3.4
floating_ip_int: 192.168.0.100
ha_host_active: host1
ha_host_active_ip_int: 192.168.0.1
ha_host_standby: host2
ha_host_standby_ip_int: 192.168.0.2



Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
