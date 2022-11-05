# Security Farm SOC
https://securityfarm.net

The Security Farm SOC consists of MediaWiki, Request Tracker, Rocket Chat and TheHive. Please look at the [documentation](https://github.com/Security-Farm/security-farm-soc/blob/main/roles/security_farm_soc/files/security_farm/security_farm_soc_documentation.pptx) for an overview. It is also availabe in /opt/security_farm/ or on the deployed wiki.

# Quickstart
[Download](https://securityfarm.net/wp-content/uploads/manual/security-farm-soc.v8.0.zip) the ESXi 6.5u3 Virtual Machine and deploy it.

Login to the host and run `security_farm_soc`, this will configure the IP amongst other things.

You _must_ use DNS in one way or another; Apache relies on the hostname passed in the HTTP request. All 5 domains must have entries pointing to the IP of the host. `security_farm_soc` will configure the machine as a DNS server for soc.lan but I imagine you'll probably just add those entries to your existing server.

Special Note: to reach the services in your browser you must use `https://`{{service}}.soc.lan. I think it's because of the tld .lan that it will try to search for it if you leave off the protocol.

All passwords (centos, database passwords, the web interface passwords, etc) _need to be changed_ if you're going to use this in production. You will need to update security_farm_soc.py backup() and restore() with said passwords. Also generate a new `$wgSecretKey` and `$wgUpgradeKey` in MediaWiki's LocalSettings.php.

Thorougly test the `security_farm_soc` backup mechanisms with data to make sure you're comfortable with them. If no attachments exist for a service you may see a restoration error for mv/chown.

The virtual machine is only provisioned to 25Gb; run `security_farm_soc` for a walkthrough on increasing the capacity.

# Version 8.0
The Security Farm SOC was always meant to be an open project, but the nature of it made it impractical for others to contribute. Now that the entire build is automated through code in v8.0 it opens up the possibility for others to contribute to the project. It also allows you to see exactly how it was configured or to deploy it on your own.

The major version number tracks with the underlying CentOS version. The minor version represents changes to the Security Farm SOC.

Given that this is a major overhaul, keep in mind that it has not yet been tested in production. Especially TheHive.

# License
GPLv3

# Author Information
Justin Mason / Security Farm PBC