request_tracker
===============

This role installs Request Tracker.

Requirements
------------

No special modules are required.

Role Variables
--------------

vars/request_tracker_vars.yml is a template for the required variables.

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

  - name: Install request_tracker
    include_role:
      name: request_tracker
    tags: [request_tracker]
```

License
-------

GPLv3

Author Information
------------------

Justin Mason / Security Farm PBC
