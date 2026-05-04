# Day 26 - Scheduled Tasks with Ansible

## Objective
Create recurring system tasks manually and automate deployment with Ansible.


## Machines Used
- gov-admin (control)
- gov-auth (managed)
- gov-app (managed)


## Commands Practiced
- crontab
- logger
- ansible-playbook


## Manual Activity

- crontab -e


Added:


*/5 * * * * logger "GovTech scheduled task running"


## Validation

crontab -l

journalctl | grep "GovTech scheduled task running"


## Ansible Automation

Deployed cron job across nodes using Ansible.


## AI Usage
Used AI to:

- validate cron syntax
- confirm correct scheduling interval


## Outcome
Recurring tasks automated across all nodes.
