# Day 07 Commands

## Disk Discovery

'''bash

lsblk

fdisk -l

'''

## Create PV

'''bash

sudo pvcreate /dev/sdb


'''

## Create VG

'''bash

sudo vgcreate gov_vg /dev/sdb

'''

## Create LV

'''bash

sudo lvcreate -L 500 -n gov_lv gov_vg

'''

## Format Filesystem 

'''bash

sudo mkfs.xfs /dev/gov_vg/gov_lv

'''

## Mount

'''bash

sudo mkdir /govdata

sudo mount /dev/gov_vg/gov_lv /govdata

'''

## Verify

'''bash

df -h

pvdisplay

vgdisplay

lvdisplay

'''

