Ansible Role: CloudFuse
=========

This deploys cloudfuse to a Linux machine, enabling you to mount your Rackspace cloudfiles container to a mount point and access them like you would any other directory/filesystem.

Requirements
------------

- A Rackspace cloud account (username + API key)

Role Variables
--------------

```
rackspace: True
openstack: False

mountpoint: /mnt/cloudfuse

rackspace_username: "test rackspace"
rackspace_api_key: "test key"

openstack_user: "test openstack"
openstack_tenant: "test tenant"
openstack_password: "test password"
```


Example Playbook
----------------

```
---
- hosts: all
  become: true
  roles:
    - cloudfuse
  vars:
    rackspace_username: username
    rackspace_api_key: xxxxxxxxxxxxxxxxxxxxxxxxx
    mountpoint: /mnt/cloudfuse
```

License
-------

GNUv3

Author Information
------------------

This role was created by [Luke Shirnia](https://shirnia.com)
