# Day 13 Troubleshooting

## Problem

SSH inaccessible.

## Diagnostics


'''bash

systemctl staus sshd

ss -tuln | grep 22

'''


## Root Causes
- sshd stopped
- firewall blocked
- bad hostname mapping

## Fix

'''bash

systemctl enable --now sshd

'''


Retested:


ssh gov-auth
