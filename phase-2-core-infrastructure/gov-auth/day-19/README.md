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
