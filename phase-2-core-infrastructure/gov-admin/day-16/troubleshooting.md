# Day 16 Troubleshooting

## Problem
HTTP service inaccessible.


## Diagnostics

On gov-app:


systemctl status httpd

ss -tuln | grep 80


On clients:

curl http://gov-app


## Root Causes
- httpd not running
- firewall blocking port 80


## Fix

systemctl enable --now httpd

firewall-cmd --permanent --add-service=http

firewall-cmd --reload


## Verification

curl http://gov-app


Returned expected HTML content.
