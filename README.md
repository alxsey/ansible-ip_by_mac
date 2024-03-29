ip_by_mac
=========

Finds IP of the device by looking up MAC addresses in `main_mac` variable.

Requirements
------------

There is few requirements on ansible (localhost) host: installed JMESPath libraries, 
arp-scan utility and ability to run arp-scan as root (in general sudo to root on localhost).

Role Variables
--------------
Role supports several variables:
`arp_scan_host` used to delegate network scanning to host. Host needs to have `arp-scan`. By default `localhost`

`arp_scan_super` user allowed to run `arp-scan` on `arp_scan_host`. Most likely `root`

`arp_scan_become_method` escalation methon on `arp_scan_host`. By default `sudo`

`arp_scan_become_password` password (if it is required) for escalation

`main_mac`list of MAC addresses. Best place to have it in Ansible Inventory

`main_mac` can be list. In this case first present IP address will be used.

Dependencies
------------
None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
    - hosts: all_pi
      roles:
         - { role: alxsey.ip_by_mac }
```
More details can be found [here](https://github.com/alxsey/ansible-ip_by_mac/tree/master/example).

License
-------

GPLv2

Author Information
------------------

Alex Ryabtsev
