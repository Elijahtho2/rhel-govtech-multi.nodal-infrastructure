# Day 22 - SELinux Contexts with Ansible

## Objective
Fix Apache SELinux context manually and enforce using Ansible.


## Machines Used
- gov-app (target)
- gov-admin (control-node)


## Commands Practiced
- semanage
- restorecon
- ansible-playbook


## Broken State Introduced
Incorrect SELinux context on /webdata.


Symptoms:
- Apache unable to serve content
- curl fails


## Manual Fix

semanage fcontext -a -t httpd_sys_content_t "/webdata(/.*)?"

restorecon -Rv /webdata


## Ansible Automation

Created playbook to enforce context across runs.


## Why It Works
SELinux requires correct context for service access.

Ansible ensures repeatable enforcement.


## AI Usage
Used AI to:

- validate SELinux syntax
- confirm recursive context patterns


## Outcome
SELinux context corrected and automated.
