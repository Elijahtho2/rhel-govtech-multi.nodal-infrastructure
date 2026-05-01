# Day 16 Commands

## On gov-app

'''bash

dnf install -y httpd

systemctl enable --now httpd


echo "GovTech Apache Server - gov-app" > /var/www/html/index.html


firewall-cmd --permanent --add-service=http

firewall-cmd --reload

'''


## On gov-admin


'''bash

curl http://gov-app

'''


## On gov-auth

curl http://gov-app

'''
