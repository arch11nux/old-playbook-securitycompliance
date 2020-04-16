Role Name
=========

A script to collect security information from a Linux host.

Requirements
------------

script roles/colsecinfo/files/colsecinfo.sh

Role Variables
--------------

N/A

Dependencies
------------

N/A

SCRIPT roles/colsecinfo/files/colsecinfo.sh
---------------------
  header
    #insert title in order to display The Begin
  
  system_info
    #target hostname info
    #search all *-release files for version info
  
  user_info
    #all root accounts (uid 0)
    #pull out vital sudoers info
    #is root permitted to login via ssh
  
  environmental_info
    #check if selinux is enabled
  
  footer
    #insert title in order to display The END
