# Day 18 Troubleshooting


## Problem
NFS mount failed.


## Diagnostics


showmount -e gov-admin

systemctl status nfs-server



## Root Causes
- service not running
- export missing
- firewall blocking


## Fix


exportfs -rav

systemctl enable --now nfs-server

firewall-cmd --reload


## Verification


mount gov-admin:/exports/share /mnt/share
