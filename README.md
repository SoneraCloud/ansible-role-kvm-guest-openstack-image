ansible-role-kvm-guest-openstack-image
======================================

Create CentOS 7 KVM guests on CentOS 7/Fedora hosts using an OpenStack image.

By default this role will download the newest CentOS7 image from http://cloud.centos.org/, create a copy-on-write clone and then start the VM.

This is still an experimental work in progress, so there are no options to specify CPU, Memory, networks etc. Pull requests very welcome!

Requirements
------------

A CentOS7 or Fedora host with enough disk, cpu and memory to launch vms.

Role Variables
--------------

This role now takes parameters from host vars and is heavily inspired by https://github.com/CSC-IT-Center-for-Science/ansible-role-provision-vm

- bootstrap_ssh_key: ssh key to deploy to vm

Optional:

- bootstrap_user: inital user to deploy ssh keys to.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-role-kvm-guest-openstack-image,
               bootstrap_ssh_key: "ssh-rsa ABCD1234" }

License
-------

MIT
