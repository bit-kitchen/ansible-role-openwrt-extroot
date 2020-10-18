ansible-role-openwrt-extroot
============================

[![Ansible Role: bit_kitchen.openwrt_extroot](https://img.shields.io/ansible/role/51332.svg)](https://galaxy.ansible.com/bit_kitchen/openwrt_extroot)
[![Build Status: bit-kitchen/ansible-role-openwrt-extroot](https://travis-ci.org/bit-kitchen/ansible-role-openwrt-extroot.svg?branch=master)](https://travis-ci.org/bit-kitchen/ansible-role-openwrt-extroot)

```sh
ansible-galaxy install bit_kitchen.openwrt_extroot
```

An ansible role that configures OpenWrt to use a storage device for external root.

Requirements
------------

None.

Role Variables
--------------

Variable   | Default | Comment
---------- | ------- | -------
overlay_device | undefined | **Required.** Example: `/dev/sda1`
auto_reboot | false | Whether to auto reboot after configuration.

Dependencies
------------

* `gekmihesg.openwrt`
* `bit_kitchen.openwrt_storage`

Example Playbook
----------------

```yml
- hosts: openwrt
  remote_user: root
  gather_facts: no
  roles:
    - name: bit_kitchen.openwrt_extroot
      overlay_device: /dev/sda1

```

License
-------

[MIT](LICENSE)

Author Information
------------------

[bit.kitchen](https://github.com/bit-kitchen)
