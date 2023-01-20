coffeesprout.openvpn-client
=========

Install OpenVPN and setup provided OpenVPN config client

Requirements
------------

Tested with Debian 11

Role Variables
--------------


    openvpn\_client\_template

The string containing the .ovpn configuration that needs to be installed; You can store this in a variable, template this or read it from a file.
See the examples

    openvpn\_packages

The packages to install for OpenVPN

    openvpn\_client_config\_name

The name for this openvpn configuration; Used in the configuration filename and the systemd unit

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

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

