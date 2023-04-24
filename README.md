coffeesprout.openvpn-client
=========

This Ansible role installs OpenVPN and sets up the provided OpenVPN client configuration.

Requirements
------------

This role has been tested with Debian 11.

Role Variables
--------------

    openvpn_client_template

This variable contains the .ovpn configuration that needs to be installed. You can store this in a variable, template it, or read it from a file.
See the examples below.

    openvpn_packages

This variable specifies the packages to install for OpenVPN.

    openvpn_client_config_name

This variable defines the name for the OpenVPN configuration. It is used in the configuration filename and the systemd unit.

Example Playbook
----------------

Below is an example of how to use this role, with variables passed in as parameters:

      - hosts: lab
        become: True
        roles:
        - role: coffeesprout.openvpn-client
          openvpn_client_template: "{{ lookup('file', '~/testkey.conf') }}"

License
-------

BSD

Author Information
------------------

