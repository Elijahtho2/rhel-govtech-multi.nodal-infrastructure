# Day 08 File Systems

## Objective
Practice formatting, mounting, and persisting filesystems.

## Machine Used
gov-admin

## Commands Practiced
- mkfs.xfs
- blkid
- mount
- umount
- mount -a
- lsblk -f

## Broken State Introduced
Lofical volume existed but lacked peristent mount.

Symptoms:
- storage disappears after reboot
- mount not persistent

## Filesystem Created

Formatted:

mkfs.xfs /dev/gov_vg/gov_lv

Mounted:

mount /dev/gov_vg/gov_lv /govdata

Retrieved UUID:

blkid

Configured persistence in:

/etc/fstab

Added:

UUID=<uuid> /govdata xfs defaults 0 0

Tested:

mount -a

## Validation
Verifed:

df -h

cat /etc/fstab

mount | grep govdata

## Why It Works
Filesystem persistence depends on fstab entries using UUID mapping.

## Multi-Node Reality
Local filesystem configuraation only affects gov-admin.

## Outcome
Persistent filesystem configured successfully.

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

