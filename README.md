Ansible Brightbox Ruby Role
===========================
[![Build Status](https://semaphoreci.com/api/v1/projects/a7b651c7-834d-49c7-b68d-39230d6110aa/461776/badge.svg)](https://semaphoreci.com/michaelrigart/ansible-role-brightbox-ruby)

An ansible role for installing the Brightbox ppa repository and installing the desired ruby version.
 
For more information, [visit the Brightbox Ruby page](http://brightbox.com/docs/ruby/ubuntu/)

Role Variables
--------------

```yaml
brightbox_ruby_psp_pkg_version: specify the specific python-software-properties version you wish to install. When specifying a version, the state will be forced to installed. When omitting the variable or leaving it empty it will install the package as specified by the state variable
brightbox_ruby_psp_pkg_state: indicates the python-software-properties package state; Allowed setting: installed, latest
brightbox_ruby_packages: list of all packages you want to install ( ruby2.2, ruby2.2-dev, ... )
brightbox_ruby_gems: list that contains additional gems you wich to install.
brightbox_ruby_gem_user_install: define if gems need to be user installed or not. This default is set to no.
```

View the default vars - defaults/main.yml - for a more detailed example.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.brightbox-ruby, brightbox_ruby_pkg_version: ruby2.1, sudo: Yes }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>
