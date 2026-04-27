# Day 11 Troubleshooting

## Problem
Node networking failed.

## Diagnostics

'''bash

ip addr

ip route

cat /etc/resolv.conf

ping -c 4 8.8.8.8

'''

## Root Cause Checked
- wrong gateway
- bad DNS
- disconnected adapter

## Fix
Validated:

NAT:

10.0.2.2

Host-only:

192.168.56.10

Reactivated connection:

nmcli con up enp0s3

## Verification

'''bash

ping -c 4 8.8.8.8

'''

