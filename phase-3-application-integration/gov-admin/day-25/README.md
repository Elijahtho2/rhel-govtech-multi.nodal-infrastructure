# Day 25 - User Security Policies with Ansible

## Objective
Create and manage users manually and automate with Ansible.


## Machines Used
- gov-auth (target)
- gov-admin (control)


## Commands Practiced
- useradd
- chage
- ansible-playbook


## Manual Activity

useradd contractor1

chage - M 30 contractor1


## Ansible Automation

Created playbook to enforce user creation and policy.


## AI Usage
Used AI to:

- generate Ansible user module usage
- validate password aging commands


## Outcome
User policy enforced and automated.
