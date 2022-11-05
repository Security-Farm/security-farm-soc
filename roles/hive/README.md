hive
====

This role installs TheHive4.

Requirements
------------

No special modules are required.

Role Variables
--------------

vars/hive_vars.yml is a template for the required variables.

Dependencies
------------

Dependent on the system_base role.

Example Playbook
----------------
```
tasks:
  - name: Install system_base
    include_role:
      name: system_base
    tags: [system_base]

  - name: Install hive
    include_role:
      name: hive
    tags: [hive]
```

License
-------

GPLv3

Author Information
------------------

Justin Mason / Security Farm PBC
