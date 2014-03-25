[![Build Status](https://travis-ci.org/Pheromone/ansible-php-cli.svg?branch=master)](https://travis-ci.org/Pheromone/ansible-php-cli)

Ansible PHP CLI
===============

Ansible role to install php-cli.

Role Variables
--------------

The role uses the following variables

- **php_cli_apt_packages**: The APT packages to install, defaults to ```[php5-cli]```.
- **php_cli_ini**: Customization for php-cli's php.ini as a list of options,
  each option is a hash using the following structure:
    - **option**: The name of the option.
    - **value**: The string value to be associated with the option.
    - **section**: Section name in INI file.


Usage
-----

    - role: php-cli
      php_cli_config:
         - option: "display_errors"
           section: "PHP"
           value: "1"
         - option: "error_reporting"
           section: "PHP"
           value: "E_ALL & ~E_NOTICE & ~E_STRICT & ~E_DEPRECATED"

License
-------

GPLv3

Author Information
------------------

Pierre Buyle <buyle@pheromone.ca>
