# Day 07 - Storage (LVM Basics)

## Objective
Practice Physical volume, volume groupe, and logical volume creation using LVM.

## Machine Used 
gov-admin

## Commands Practiced
- lsblk
- fdisk
- pvcreate
- vgcreate
- lvcreate
- lvdisplay
- vgdisplay
- pvdisplay
- mkfs.xfs
- mount

## Broken State Introduced
Secondary disk initially uncofigured.

Symptoms:

- no physical volume
- no volume group
- no logical volume
- no mounted storage available

## Storage Configuration

Created physical volume:

pvcreate /dev/sdb

Created volume group:

vgcreate gov_vg /dev/sdb

Created logical volume:

lvcreate -L 500M -n gov_lv gov_vg

Created filesystem:

mkfs.xfs /dev/gov_vg/gov_lv

Created mount point:

mkdir /govdata

Mounted volume:

mount /dev/gov_vg/gov_lv /govdata

## Validation
Verified:

lsblk

df -h

lvdisplay

vgdisplay

pvdisplay

## Why It Works
LVM layers:

Disk

-> Physical Volume

-> Volume Group

-> Logical Volume

-> Filesystem

-> Mount Point

## Multi-Node Reality
Storage configuration exists only on gov-admin.

Nothing propagates to gov-auth or gov-app.

## Outcome
Successfully built working LVM storage stack.

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
 
