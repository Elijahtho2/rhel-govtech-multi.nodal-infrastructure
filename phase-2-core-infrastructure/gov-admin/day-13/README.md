# Day 13 - SSH Client and Server

## Objective
Configure secure remote shell connectivity between nodes.

## Commands Practiced
- systemctl

- ssh

- sshd


Enable service:


systemctl enable --now sshd


Validated:


systemctl status sshd


## Connectivity Tested


From gov-admin:

ssh gov-auth

ssh gov-app


From gov-auth

ssh gov-admin


From gov-app:

ssh gov-admin


## Why It Works
sshd accepts remote encrypted shell sessions.

## Outcome
Remote shell access operational across nodes.


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

