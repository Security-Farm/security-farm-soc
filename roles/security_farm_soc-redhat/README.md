security_farm_soc
=================

This role installs the Security Farm SOC onto an Alma 10 minimal installation with qemu-guest-agent.

Recommended Partitions for a VM:
/boot/efi - 600 MiB
/boot     - 1024 MiB
/swap     - 4 GiB
/         - The Rest

All I do once the build is complete is run `security_farm_soc.py` to configure the system and restore the default backups. Then I templatize the vm and remove the user I created for ansible.


Requirements
------------

No special modules are required.

Role Variables
--------------

vars/security_farm_soc_vars.yml contains the variables needed to successfully build. system_base also contains some default variables for itself.  

Copy security_farm_soc_vars.yml to a location that won't get synchronized to git and create new passwords if you want to avoid doing that after the machine is setup.

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
