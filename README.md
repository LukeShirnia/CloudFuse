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

rackspace_username: "rackspace_username"
rackspace_api_key: "rackspace_api_key"

openstack_user: "openstack_user"
openstack_tenant: "openstack_tenant"
openstack_password: "openstack_password"
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
