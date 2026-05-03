# Day 23 - SELinux Troubleshooting with Ansible

## Objective
Break SELinux intentionally and fix manually and with automation.


## Machines Used
- gov-app (target)
- gov-admin (control)


## Broken State Introduced

chcon -t user_home_t /webdat/index.html


Symptoms:
- Apache fails
- curl returns error


## Diagnostics

ausearch -m AVC -ts recent

ls -Z /webdata/index.html


## Manual Fix

restorecon -Rv /webdata


## Ansible Fix

Playbook created for remediation.


## AI Usage
Used AI to:
- interpret AVC logs
- determine correct remdiation


## Outcome
SELinux denial resolved manually and automated.
