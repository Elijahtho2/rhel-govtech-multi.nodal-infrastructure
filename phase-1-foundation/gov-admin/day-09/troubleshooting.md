# Day 09 Troubleshooting

## Risk
Incorrect fstab can break mounts.

## Diagnostics

'''bash

mount -a

blkid

cat /etc/fstab

'''

## Root Cause Tested
Potential UUID mismatch or mount failure.

## Verification

'''bash

df -h

mount | grep govdata

'''

Mount survived reboot successfully.
