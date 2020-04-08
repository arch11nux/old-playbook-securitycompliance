ansible-playbook -i hosts securitycompliance.yml --syntax-check


- hosts: esxcentos
  roles:
  - selinux

$ ansible-galaxy init roles/selinux