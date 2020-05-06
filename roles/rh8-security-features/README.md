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

How is working:
===============
# Just check: 
  # variable var_go_execute = False (roles/rh8-security-features/defaults/main.yml)
  ansible-playbook securitycompliance.yml -i hosts --ask-become-pass  --tags "rh8-security-features"
  - genarate a local report on each server (~report.out)

# check & apply: 
  # variable var_go_execute = True (roles/rh8-security-features/defaults/main.yml)
  ansible-playbook securitycompliance.yml -i hosts --ask-become-pass  --tags "rh8-security-features"
  - genarate a local report on each server (~report.out)


Structure:
==========
roles/rh8-security-features
  defaults/main.yml
  templates/report.j2
  tasks/main.yml
    tasks/fapolicyd.yml
    tasks/crypto-policies.yml
    tasks/firewalld.yml
    tasks/selinux.yml
    tasks/linenum.yml
    tasks/auditd.yml
    tasks/obsolete-services.yml

TAGS:
=====
- rh8-security-features
- redhat8
# every task inside the role have it's own TAG
  - fapolicyd
  - crypto-policies
  - firewalld
  - selinux
  - linenum
  - auditd
  - obsolete-services