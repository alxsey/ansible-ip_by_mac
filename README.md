ip_by_mac
=========

Finds IP of the device by looking up 

Routers are identified by MAC addresses in main_mac variable.

Requirements
------------

There is few requirements on ansible (localhost) host: installed JMESPath libraries, 
arp-scan utility and ability to run arp-scan as root (in general sudo to root on localhost).

Role Variables
--------------

By default

Dependencies
------------
None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all_pi
      roles:
         - { role: alxsey.ip_by_mac }

License
-------

GPLv2

Author Information
------------------

Alex Ryabtsev
