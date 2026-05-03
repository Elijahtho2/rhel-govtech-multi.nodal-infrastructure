# Day 21 - SELinux Basics with Ansible Validation

## Objective
Control SELinux modes manually and validate enforcement across nodes using Ansible.


## Machines Used
- gov-admin (control node)
- gov-auth (managed)
- gov-app (managed)


## Manual Activity

On all nodes: 


getenforce

setenforce 0

getenforce

setenforce 1

getenforce


## Broken State Introduced
SELinux switched to permissive mode.


Symptoms:
- system not enforcing policies 
- reduced security enforcement


## Troubleshooting Performed

Verified SELinux mode:


getenforce

sestatus


## Ansible Validation

From gov-admin:


ansible all -i ~/ansible/inventory -m command -a "getenforce"


## Why It Works
SELinux controls mandatory access

Ansible allows centralized validation across all nodes


## AI Usage
Used AI to confirm:
- confirm SELinux behavior
- SELinux mode meanings
- expected outputs for enforcing vs. permissive


## Multi-Node Reality
Each node enforces SELinux independently but can be validated centrally.


## Outcome
SELinux mode controlled manually and validated across all nodes via Ansible.
