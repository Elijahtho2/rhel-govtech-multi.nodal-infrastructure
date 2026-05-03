# Day 19 Troubleshooting

## Problem
Mount not persistent.


## Root Cause
Missing fstab entry.


## Fix


Added NFS entry to /etc/fstab.


## Verification


df -h 

mount | grep share
