ansible-role-openwrt-extroot
============================

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
