system_base
=========

Configure target hosts to the baseline configuration.

Currently enables automatic security updates but some of these updates may need a manual reboot to take effect. On CentOS 7 run `needs-restarting -r` and on CentOS 8 `dnf needs-restarting` to check.

Requirements
------------

No special modules are required.

Role Variables
--------------

See /defualts/main.yml and vars/main.yml

Dependencies
------------

This is the baseline role for all systems thus it has no dependencies, but is potentially depended on by all future roles.

Example Playbook
----------------
```
tasks:
  - name: Install system_base
    include_role:
      name: system_base
    tags: [system_base]
```

License
-------

GPLv3

Author Information
------------------

Justin Mason / Security Farm PBC
