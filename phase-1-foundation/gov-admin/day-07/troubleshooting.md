# Day 07 Troubleshooting

## Problem
No usable LVM storage existed

## Symptoms
- no mounted volume
- no logical volume present

## Diagnostics

'''bash

lvblk

pvdisplay

vgdisplay

lvdisplay

'''

## Root Cause
Disk had not been initialized for LVM

## Fix 

'''bash

pvcreate /dev/sdb

vgcreate gov_vg /dev/sdb

lvcreate -L 500M -n gov_lv gov_vg

mkfs.xfs /dev/gov_vg/gov_lv

mount /dev/gov_vg/gov_lv /govdata

'''

## Verification

'''bash

df -h

lvdisplay

'''

Storage available and mounted
