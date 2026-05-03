# Day 19 - NFS Automount

## Objective
Make NFS mount persistent cross reboots.

## Configuration

Edited /etc/fstab:


gov-admin:exports/share /mnt/share nfs defaults,_netdev 0 0


Tested:


mount -a


Rebooted system.


## Validation


df -h

mount | grep share


## Outcome

NFS persists across reboots.


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

