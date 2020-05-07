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
  # SET the variable var_check_mode = True (roles/rh8-security-features/defaults/main.yml)
  ansible-playbook securitycompliance.yml -i hosts --ask-become-pass  --tags "rh8-security-features"
  - genarate a local report on each server (~report.out)

# check & apply *** D A N G E R ***: 
  # SET the variable var_check_mode = False (roles/rh8-security-features/defaults/main.yml)
  ansible-playbook securitycompliance.yml -i hosts --ask-become-pass  --tags "rh8-security-features"
  - genarate a local report on each server (~report.out)

NOTE:
=====
playbook exemple, when you call the role:

# Ansible Playbook - check Security Compliance on Linux servers 
- name: "Playing with Ansible"
  hosts: servers
  port: 22
  gather_facts: true
  tasks:
  - name: "rh8-security-features"
      # role rh8-security-features: Security for RHEL8 | Linux RH8
    include_role:
      name: rh8-security-features
    tags:
      - RedHat8
      - rh8-security-features
    when: >
      (ansible_facts['distribution'] == "RedHat" and ansible_facts['distribution_major_version'] == "8")

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