[![Build Status](https://travis-ci.org/CSC-IT-Center-for-Science/ansible-role-shibboleth-sp.svg?branch=master)](https://travis-ci.org/CSC-IT-Center-for-Science/ansible-role-shibboleth-sp)

Ansible-Role: Shibboleth SP
=========

An role which installs Shibboleth SP on RedHat/Debian servers.

Requirements
------------

* cmprescott.xml ( Mandatory )
* CSC-IT-Center-for-Science.apache ( Optional but suggested )

This Role installs shibboleth-sp if not already installed and configures some defaults options. Also Debug can be switched [On/Off].

Role Variables
--------------

See defaults/main.yml for the variables you can overwrite via role call via parameter
* shibboleth_state: latest
* shibboleth_debug: [ true / false ]

shibboleth2.xml default configuration
* shibboleth_signing: front
* shibboleth_encryption: false
* shibboleth_handlerssl: true
* shibboleth_redirectLimit: exact
* shibboleth_cookieprops: https

Dependencies
------------

cmprescott.xml

Example Playbook
----------------

    - hosts: localhost
      roles:
        - { role: CSC-IT-Center-for-Science.shibboleth-sp }

