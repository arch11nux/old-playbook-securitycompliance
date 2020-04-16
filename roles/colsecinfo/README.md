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
    #current umask value with both octal and symbolic output
    #umask value as in /etc/login.defs
  
  interesting_files
    #search for suid files (perm 4000)
    #list of 'interesting' suid files - feel free to make additions
    #lists world-writable suid files
    #lists world-writable suid files owned by root
    
  footer
    #insert title in order to display The END
