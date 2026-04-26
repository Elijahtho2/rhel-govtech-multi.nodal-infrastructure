# Day 08 Troubleshooting

## Problem
Storage not persistent.

## Symptoms 
Mount would disappear after reboot.

## Diagnostics

'''bash

df -h 

cat /etc/fstab

blkid

'''

## Root Cause

No persistent mount entry.

## Fix 

'''bash

vim /etc/fstab

mount -a

'''

## Verification

'''bash

mount | grep govdata

'''

Filesystem persisted successfully.
