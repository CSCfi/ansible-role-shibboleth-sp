[![Build Status](https://travis-ci.org/CSCfi/ansible-role-shibboleth-sp.svg?branch=master)](https://travis-ci.org/CSCfi/ansible-role-shibboleth-sp)

Ansible-Role: Shibboleth SP
=========

An role which installs Shibboleth SP on RedHat/Debian servers.

Disclaimer
---

This is an example of a role to deploy SAML Service Provider to e.g. Haka user authentication federation. The deployer is responsible for making sure that the end result complies with requirements in each federation. Authors of the role don't take a stand on whether the end result is compliant or not.

Requirements
------------

* cmprescott.xml ( Mandatory )
* CSCfi.apache ( Optional but suggested )

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

    - hosts: all
      roles:
        - { role: CSCfi.shibboleth-sp }

