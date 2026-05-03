# Ansible Automation Overview

## Control Node
gov-admin


## Managed Nodes
- gov-auth
- gov-app


## Purpose
Automate system administration tasks across multiple nodes.


## Usage

Run commands:


ansible all -i inventory -m ping


Run playbooks:


ansible-playbook -i inventory playbooks/<file>.yml


## AI Integration
AI was used to:
- generate playbooks
- troubleshoot syntax errors
0 validate module usage
- accelerate command construction


## Outcome
Infrastructure tasks transitioned from manual execution to automated orchestration.
