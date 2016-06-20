[![Open AS Communication Gateway](https://openas.org/assets/img/logo.png)](https://openas.org) 
## Open AS Communication Gateway

An open, integrated, easy-to-use, GUI-managed SMTP gateway scanning your emails for spam and viruses.

The Open AS Communication Gateway (or short 'AS') aims to be a all-in-one solution of an SMTP gateway: It accepts incoming email, performs various antispam-related processes like blacklisting, virus- and spam-scanning, and relays the mails to pre-defined SMTP servers. It's built upon an Ubuntu Server system, and can be entirely managed via a user-friendly web-frontend.

:warning: This branch is currently **UNSTABLE** and supports Ubuntu 14.04 LTS **ONLY**! :warning:

Main features
----------------------------------------

 * Recipient maps (specified manualy or fetched via LDAP, e.g. from MS AD)
 * White- and black-listing based on e-mail addresses, hostnames, domain-names, network ranges, CIDR ranges, reverse lookups and so on
 * Remote blacklisting (DNSBLs, URI DNSBLs, etc.)
 * Greylisting
 * Spam-scanning and scoring
 * Virus-scanning
 * Attachment scanning
 * Dynamic "Score Matrix", which lets you define what to do with mails from a certain origin, to what extent, at what score, etc.
 * End-User-maintainable email quarantining
 * A very pretty, user-friendly web GUI

Installation
----------------------------------------

On a fresh Ubuntu 14.04 LTS box type:

	sudo add-apt-repository -y ppa:open-as-team/ppa
	sudo apt-get update && sudo apt-get upgrade
	sudo apt-get -q -y install open-as-cgw

Please make sure to read the docs at https://wiki.openas.org.

Developers
----------------------------------------

Fork the repo and set-up a local development environment by executing

	/bin/bash ./lib/bin/set_dev_environment.sh

To start the GUI in development mode type:

	/usr/bin/perl ./gui/script/limesgui_server.pl

from within your local copy of the repositoy.

This will start a local webserver for accessing the GUI.
All changes on the code will be visible immediatly.


You can also test the current version from the master branch.
Use the command below on a fresh Ubuntu box:

	sudo bash -c "$(curl -sL openas.org/install-devel.sh)"

Ubuntu PPA Packages are built daily at midnight via launchpad.net.

Resources
----------------------------------------
* Website: https://openas.org
* Forum:   https://forum.openas.org
* Wiki:    https://wiki.openas.org

Build Status
----------------------------------------

[![Travis CI](https://travis-ci.org/open-as-team/open-as-cgw.svg?branch=master)](https://travis-ci.org/open-as-team/open-as-cgw)

