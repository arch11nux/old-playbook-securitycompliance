Security Compliance (CIS and non CIS)

Ansible Security Compliance playbook
This profile configures Red Hat Enterprise Linux 7 to the Security Compliance

How to apply this remediation role:
ansible-playbook -i hosts securitycompliance.yml

Requirements
Ansible version 2.5 or higher

Role
  - ctrlselinux
  - ctrlnist800

Dependencies
N/A

TAGS informations
  cis = des contrôles SELinux qui sont dans le CIS
  noncis = des contrôles SELinux qui ne sont pas dans le CIS
  rh7 = relier au RedHat version 7


