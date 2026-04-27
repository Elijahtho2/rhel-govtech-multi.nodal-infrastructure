# Day 11 Commands

## On Each VM

'''bash

hostname

ip addr

ip route

nmcli con show

cat /etc/resolv.conf

ping -c 4 8.8.8.8

'''

## Optional DNS Fix

'''

nmcli con mod enp0s3 ipv4.dns 8.8.8.8

nmcli con up enp0s3

'''

## Verify Gateway

'''bash

ip route

'''

Expected NAT gatway often:

10.0.2.2
