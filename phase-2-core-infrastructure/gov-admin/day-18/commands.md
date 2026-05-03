# Day 18 Commands

## On gov-admin

'''bash

dnf install -y nfs-utils

mkdir -p /exports/share

chmod 777 /exports/share


echo "/exports/share 192.168.56.0/24(rw,sync,no_root_squash)" >> /etc/exports


exportfs -rav

systemctl enable --now nfs-server


firewall-cmd --permanent --add-service=nfs

firewall-cmd --reload

'''



## On gov-auth & gov-app

'''bash

dnf install -y nfs-utils

mkdir /mnt/share

mount gov-admin:/exports/share /mnt/share

df -h

'''
