# Day 20 - System Logging


## Objective
Use journald to inspect logs and generate custom log entries.


## Commands Practiced
- journalctl
- logger


## Activity


Viewed logs:


journalctl -xe


Service logs:


journalctl -u sshd

journalctl -u httpd


Generated test log:


logger "GovTech log test"


## Validation


journalctl | grep GovTech


## Outcome
Logs successfully generated and reviewed.


## Automation Opportunity

This task can be automated using Ansible.

Future automation includes:
- remote execution across nodes
- configuration enforcement
- repeatable deployment


## AI Usage 

AI was used to:
- validate commands
- troubleshoot issues
- confirm expected outputs

