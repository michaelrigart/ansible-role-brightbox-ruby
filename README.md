Ansible Brightbox Ruby Role
===========================

An ansible role for installing the Brightbox ppa repository and installing the desired ruby version.
 
For more information, [visit the Brightbox Ruby page](http://brightbox.com/docs/ruby/ubuntu/)

Role Variables
--------------

- brightbox_ruby_psp_pkg_version: specify the specific python-software-properties version you wish to install
When specifying a version, the state will be forced to installed. When omitting the variable or leaving it empty
it will install the package as specified by the state variable
- brightbox_ruby_psp_pkg_state: indicates the python-software-properties package state; Allowed setting: installed, latest
- brightbox_ruby_pkg_version: you can specify which ruby version you which to install. Either use the short version (eg. 2.1) for the 
latest 2.1 version, or specify the full version name (eg. ruby2.1=2.1.2-1bbox1~trusty2).
- brightbox_ruby_gems: list that contains additional gems you wich to install.

View the default vars - defaults/main.yml - for a more detailed example.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: michaelrigart.brightbox_ruby, brightbox_ruby_pkg_version: ruby2.1 }

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>