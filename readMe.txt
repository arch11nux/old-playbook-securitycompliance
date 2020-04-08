ansible-playbook -i hosts securitycompliance.yml --syntax-check


- hosts: esxcentos
  roles:
  - selinux


# informations sur les TAGS
cis = des contrôles SELinux qui sont dans le CIS
rh7 = relier au RedHat version 7