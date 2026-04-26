# Day 09 - Persistent Storage 

## Objective 
Validate storage survives reboot and fstab is correct.

## Machine Used 
gov-admin

## Commands Practiced 
- reboot 
- mount
- df
- lsblk
- cat /etc/fstab

## Broken State Tested
Potential boot mount failure scenario.

## Validation Performed

Checked:

cat /etc/fstab

Tested:

mount -a

Rebooted: 

reboot

Post-reboot validation:

df -h

mount | grep govdata

lsblk -f

## Why It Works
fstab UUID mapping automatically mounts at boot.

## Multi-Node Reality
Storage persistence remains local to gov-admin.

## Outcome
Verified reboot persistence successfully.
