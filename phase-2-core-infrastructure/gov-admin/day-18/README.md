# Day 18 - NFS Network Storage

## Objective
Export shared storage from gov-admin to other nodes.

## Objective
Export shared storage from gov-admin to other nodes.


## Machines Used
- gov-admin (server)
- gov-auth (client)
- gov-app (client)


## Commands Practiced
- dnf install
- exportfs
- mount
- systemctl


## Configuration

On gov-admin:


dnf install -y nfs-utils

mkdir -p /exports/share

chmod 777 /exports/share



Added export:


echo "/exports/share 192.168.56.0/24(rw,sync,no_root_squash)" >> /etc/exports


exports -rav

systemctl enable --now nfs-server


Opened firewall:


firewall-cmd --permanent --add-service=nfs

firewall-cmd --reload


On clients:


dnf install -y nfs-utils

mkdir /mnt/share

mount gov-admin:/exports/share /mnt/share


## Validation

df -h


## Outcome
Shared storage available across nodes.
