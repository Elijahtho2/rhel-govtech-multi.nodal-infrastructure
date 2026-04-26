# Day 08 Commands

## Check Filesystem

'''bash

lsblk -f

'''

## Format

'''bash

mkfs.xfs /dev/gov_vg/gov_lv

'''

## Mount

'''bash

mkdir /govdata

mount /dev/gov_vg/gov_lv /govdata

## Get UUID

'''bash

blkid

'''

## Configure Persistence

'''bash

vim /etc/fstab

'''

Add:

'''bash

UUID=<uuid> /govdata xfs defaults 0 0

'''

## Test

'''bash

mount -a

df -h

'''
