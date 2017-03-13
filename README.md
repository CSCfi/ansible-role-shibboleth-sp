Ansible-Role: Shibboleth SP
=========

An role which installs Shibboleth SP on RedHat/Debian servers.

Requirements
------------

* cmprescott.xml ( Mandatory )
* CSC-IT-Center-for-Science.apache ( Optional but suggested )

This Role installs apache web server if not already installed, but doesnt perform any configuration for it.

Role Variables
--------------

See defaults/main.yml for the variables you can overwrite via role call as parameter

shibboleth_state: latest
shibboleth_debug: [ true / false ]

shibboleth2.xml default configuration

shibboleth_signing: front
shibboleth_encryption: false
shibboleth_handlerssl: true
shibboleth_redirectLimit: exact
shibboleth_cookieprops: https

Dependencies
------------

cmprescott.xml

Example Playbook
----------------

    - hosts: apache
      roles:
        - { role: CSC-IT-Center-for-Science.shibboleth-sp }

