# Day 12 Commands

## On All Three VMs

Edit:

'''bash

sudo vim /etc/hosts

'''


Add:


'''

'''bash

192.168.56.10 gov-admin

192.168.56.20 gov-auth

192.168.56.30 gov-app

'''


Test:


'''bash

ping -c 4 gov-admin

ping -c 4 gov-auth

ping -c 4 gov-app

'''
