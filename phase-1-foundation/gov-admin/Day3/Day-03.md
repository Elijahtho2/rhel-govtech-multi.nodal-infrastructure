# Day 03 - ACLs

*** Gov-Admin VM
## Objectives

- Extend Permission model using ACLs
- Allow non-group user access

### Commands:

dnf install -y acl

setfacl -m u:user400:rwx /sharedgroup

setfacl -d u:user400:rwx /sharedgroup

getfacl /sharedgroup

# Broken

- user400 still cannot write

## Troubleshoot

### Commands

getfacl /sharedgroup

------screenshot---------

# Fixed

### Commands:

setfacl -d -m u:user400:rwx /sharedgroup

----Screenshot----

*** Gov-Auth VM

### Commands:

su - user400

touch /sharedgroup/acl-test

*** Gov-App VM

- Validate inheritance:

### Commands:

touch /sharedgroup/app-test


