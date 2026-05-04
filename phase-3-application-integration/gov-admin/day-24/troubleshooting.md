# Day 24 Troubleshooting

## Problem
Apache not reachable on new port.


## Diagnostics

ss -tuln | grep 8080

firewall-cmd --list-all


## Root Cause
Port not allowed in SELinux or firewall.


## Fix

semange port -a -t http_port_t -p tcp 8080

firewall-cmd --reload


## Verification

curl http://gov-app:8080
