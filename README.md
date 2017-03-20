ansible-basic-server-setup
=========

A role to do basic setup of a debian based server. This role will install
essential packages and do basic security.

Requirements
------------

None.

Role Variables
--------------

By default, this role will install the following packages:

* build-essential
* git-core
* python-setuptools
* python-software-properties
* python-pip
* aptitude
* fail2ban
* unattended-upgrades
* vim

You can specify additional packages to install by setting the variable
`additional_packages_to_install` to a list of additional packages to install.

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: webservers
  roles:
    - role: ansible-basic-server-setup
      additional_packages_to_install:
        - postgresql-server
        - nodejs
        - ruby
```

Author
------

Rick Apichairuk

