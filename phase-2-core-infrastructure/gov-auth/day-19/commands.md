# Day 19 Commands

'''bash

vim /etc/fstab

'''


Add:


'''bash

gov-admin:/exports/share /mnt/share nfs defaults,_netdev 0 0

'''


Test:


'''bash

mount -a

df -h

reboot

'''


After reboot:


'''bash

df -h

mount | grep share

'''
