iris
=========

This role installs DFIR-IRIS

Requirements
------------

No special modules are required.

Role Variables
--------------

vars/iris_vars.yml is a template for the required variables.

Dependencies
------------

Dependent on the system_base role.

Example Playbook
----------------
```
- name: Install system_base
  include_role:
    name: system_base
  tags: [system_base]

- name: Install iris
  include_role:
    name: iris-redhat
  tags: [iris]
```

License
-------

GPLv3

Author Information
------------------

Justin Mason / Security Farm PBC
