Role Name
=========

A brief description of the role goes here.

Requirements
------------

On the target systen `udev` should be installed.

Role Variables
--------------

Default values:

```yaml
ns: apple-bluetooth-keyboard
pfx: /opt
repo_dst: "{{pfx}}/{{ns}}"
repo_user: root
repo_group: root
repo_url: https://github.com/ckuelker/apple-bluetooth-keyboard.git
rules: /etc/udev/rules.d/90-apple-bluetooth-keyboard.rules
```

- __ns__: Name Space
- __pfx__: Prefix, change it to an existing directory
- **repo_dst**: Repository destination directory (will be created)
- **repo_user**: Admin user or root.
- **repo_group**: Admin group or root
- **repo_url**: Repository URL for the `udev` rule
- __rules__: Target for the `udev` rule

From this variables only **repo_user** and **repo_group** is likely to
be changed to a local user.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role

    - hosts: localhost
      roles:
         - { role: apple-bluetooth-keyboard }

License
-------

GPLv3

Author Information
------------------

This role was created in 2024 by [Christian Külker](https://christian.kuelker.info)

