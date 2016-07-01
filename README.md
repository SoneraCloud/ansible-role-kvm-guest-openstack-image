ansible-role-kvm-guest-openstack-image
======================================

Create CentOS 7 KVM guests using an OpenStack image.

By default this role will download the newest CentOS7 image from http://cloud.centos.org/, create a copy-on-write clone and then start the VM.

This is still an experimental work in progress, so there are no options to specify CPU, Memory, networks etc. Pull requests very welcome!

Requirements
------------

A CentOS7 or Fedora host with enough disk, cpu and memory to launch vms.

Role Variables
--------------

- guest_name is the name that the new vm will take.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: kvm-guest-create, guest_name: 'example' }

License
-------

MIT
