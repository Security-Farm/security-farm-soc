rocket_chat
===========

This role installs Rocket Chat.

Requirements
------------

No special modules are required.

Role Variables
--------------

vars/rocket_chat_vars.yml is a template for the required variables.

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

  - name: Install Rocket Chat
    include_role:
      name: rocket_chat
    tags: [rocket_chat]
```

License
-------

GPLv3

Author Information
------------------

Justin Mason / Security Farm PBC
