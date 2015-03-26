Ansible PHP Role
=================
[![Build Status](https://travis-ci.org/michaelrigart/ansible-role-php.svg?branch=master)](https://travis-ci.org/michaelrigart/ansible-role-php)

An ansible role for installing and configuring PHP.

This role installs and configures PHP. You can define a custom ppa if you like.

For more information on PHP, [visit the PHP website](http://www.php.net)

Role Variables
--------------

```yaml
php_ppa_repo: the ppa address if you wish to install from a ppa
php_packages: list of php packages you want to install
php_service: service you want to restart after config changes
php_mods_path: path to php module files
php_config_files: list where each element is a dict. The dict holds the location, filename and parameters for the needed config files
php_disable_mods: list where each element is a dict. Holds the location of the modules to disable and a list of all module names
php_enable_mods: list where each element is a dict. Holds the location of the modules to enable and a list of dicts containing the module name and load priority
```

View the default vars - defaults/main.yml - for a more detailed example.

Example Playbook
-------------------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.php, sudo: Yes }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>