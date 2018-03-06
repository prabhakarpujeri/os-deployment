racadm-deployment
=========

Ansible Role helps in OS deployment on PERC, ISCSI, FCoE, FC, SW RAID, onboadSATA.
it also provide BIOS, PERC, NIC configuration configiration 

Requirements
------------
currently is support on RHEL, SLES system from where you can execute racadm command


Role Variables
--------------
idracadm_user: root
idracadm_password: calvin
idracadm_hosts:
  - 100.98.4.22
share_user: dummy
share_password: dummy
share_iso_path: "//100.98.4.4/public/test/automation/new_f27.iso"

redhat:
  packages:
    - openssl-devel
    - srvadmin-idracadm

env:
  PATH: "{{PATH}}:/opt/dell/bin"  
  
Dependencies
------------

TBD

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: racadm-deployment }

License
-------

BSD

Author Information
------------------

TBD
