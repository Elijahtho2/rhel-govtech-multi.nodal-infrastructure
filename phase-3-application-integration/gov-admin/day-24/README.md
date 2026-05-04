# Day 24 - Secure Services with Ansible

## Objective
Configure Apache on custom port with SELinux and firewall using Ansible.


## Machines Used
- gov-app (server)
- gov-admin (control)
- gov-auth (client)


## Broken State Introduced
Apache fails when port changed.


## Configuration

Changed Apache port to 8080.


## Anshible Automation

Configured:
- Apache port
- SELinux port allowance
- firewall rule


## AI Usage
Used AI to:
- validate SELinux port mapping
- confirm fiewall commands


## Outcome
Apache running securely on custom port.
