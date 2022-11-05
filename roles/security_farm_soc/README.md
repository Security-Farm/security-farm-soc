security_farm_soc
=================

This role installs the Security Farm SOC onto a CentOS 8 Stream Minimal installation w/Guest Agents.

Recommended Partitions for a VM:
/home - deleted
/boot - 1024 MiB
/swap - 4 GiB
/     - The Rest

All I do once the build is complete is run `security_farm_soc.py` to restore the default backups, configure the system and then check the status to make sure all is well.


Requirements
------------

No special modules are required.

Role Variables
--------------

vars/security_farm_soc_vars.yml contains the variables needed to successfully build. system_base also contains some default variables for itself.

Dependencies
------------

Dependent on the following roles: system_base, mediawiki, request_tracker, rocket_chat, hive

Example Playbook
----------------

Use build-security-farm-soc.yml

License
-------

GPLv3

Author Information
------------------

Justin Mason / Security Farm PBC
