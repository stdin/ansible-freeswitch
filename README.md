ansible-freeswitch
=========

[![Build Status](https://travis-ci.org/stdin/ansible-freeswitch.svg)](https://travis-ci.org/mwolff44/freeswitch-mw)
[![Galaxy](http://img.shields.io/badge/galaxy-stdin.ansible-blue.svg?style=flat-square)](https://galaxy.ansible.com/stdin/freeswitch/)


Install and configure FreeSwitch 1.6 using packages.

Supported OS
--------------

- Debian 8 Jessie
- Ubuntu 14.04 Trusty
- Ubuntu 16.04 Xenial (experimental)


Role Variables
--------------

#### Install modules

	freeswitch_install_modules:  # FreeSwitch modules to install
	  - xml-curl
	  - python

#### Enable modules

	freeswitch_enable_modules:  # FreeSwitch modules to enable
	  - mod_xml_curl
	  - mod_python


Example Playbook
----------------

    - hosts: freeswitch-servers
      become: true
      roles:
        - role: stdin.ansible-freeswitch
          freeswitch_install_modules:
            - xml-curl
            - python
          freeswitch_enable_modules:
            - mod_xml_curl
            - mod_python

License
-------

MIT

Author
------------------

Slava Yanson <sy@apeiron.io>
https://apeiron.io/
