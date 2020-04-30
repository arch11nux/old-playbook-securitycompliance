Role Name: rh8-security-features
=========

This role install and configure RHEL8 security. The role is composed from many subcategorys. By default all subcategorys are set to "no execute"

Requirements
------------

RHEL8

Role Variables
--------------

var_go_execute = False (roles/rh8-security-features/defaults/main.yml)

Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - rh8-security-features
            default
              - main.yml
            tasks
              - main.yml
              - fapolicyd.yml
