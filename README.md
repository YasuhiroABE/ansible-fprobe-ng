Role Name: fprobe-ng
=========

This role sets up the fprobe-ng package on Ubuntu or Debian.

Requirements
------------

This role was tested on the following platforms.

### Ansible
- Version 2.4

### Distributions
- Ubuntu 16.04
- Debian 9

Role Variables
--------------

### Defaults
* fprobe_default_config_file: '/etc/default/fprobe'
  * This file should contains lines beggning with INTERFACE and FLOW_COLLECTOR.

* fprobe_collector_ipaddr: '127.0.0.1'
  * Either iP address or hostname for the destination address of FLOW collector

* fprobe_collector_port: '2055'
  * The destination port number of FLOW collector

* fprobe_probe_ethdev: 'eth0'
  * Local network device name, such as 'eth0' and 'enp1s0'

Dependencies
------------

N/A

Example Playbook
----------------

    - hosts: all
      vars:
        - fprobe_service_ethdev: 'enp1s0'
      roles:
        - yasuhiroabe.fprobe-ng

License
-------

Apache License 2.0

Author Information
------------------

[Yasuhiro ABE](http://www.yasundial.org/foaf.xml)

