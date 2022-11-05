mediawiki
=========

This role installs MediaWiki

Requirements
------------

No special modules are required.

Role Variables
--------------

vars/mediawiki_vars.yml is a template for the required variables.

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

- name: Install MediaWiki
  include_role:
    name: mediawiki
  tags: [mediawiki]
```

License
-------

GPLv3

Author Information
------------------

Justin Mason / Security Farm PBC
