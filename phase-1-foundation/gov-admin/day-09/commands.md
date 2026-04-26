# Day 09 Commands

## Pre-Reboot Checks

'''bash

cat /etc/fstab

mount -a

df -h

'''

## Reboot

'''bash

reboot

'''

## After Reboot

'''bash

df -h

mount | grep govdata

lsblk -f

'''
