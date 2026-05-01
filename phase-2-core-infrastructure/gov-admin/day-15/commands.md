# Day 15 Commands

## Start Firewalld

'''bash

systemctl enable --now firewalld

'''


## Verify

'''bash

firewall-cmd --state

firewall-cmd --list-all

'''


## Allow HTTP

'''bash

firewall-cmd --permanent --add-service=http

firewall-cmd --reload

'''


## Verify

'''bash

firewall-cmd --list-all

'''
