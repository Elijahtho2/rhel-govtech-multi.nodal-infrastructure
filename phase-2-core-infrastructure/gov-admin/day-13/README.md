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
