Security Compliance (CIS and non CIS)

Ansible Security Compliance playbook
This profile configures Red Hat Enterprise Linux 7 to the Security Compliance

How to apply this remediation role:
ansible-playbook securitycompliance.yml -i hosts --ask-vault-pass

Requirements
Ansible version 2.5 or higher

Role
  - sec001
  - sec002
  - sec003
  - rh8-security-features

Dependencies
N/A

TAGS informations
  cis = des contrôles SELinux qui sont dans le CIS
  noncis = des contrôles qui ne sont pas dans le CIS
  nist-800 = des contrôles nist-800
  rhel7 = relier au RedHat version 7
  rhel8 = relier au RedHat version 8
  LinEnum = POSIX capabilities
