# Day 11 - Networking Basics

## Objective
Configure and validate IP addressing, routes and DNS across all nodes.

## Machines Used
- gov-admin
- gov-auth
- gov-app

## Commands Practiced 
- ip addr
- ip route
- nmcli
- ping
- cat /etc/resolv.conf

## Broken State Introduced
Potential issues introduced:

- incorrect gateway
- missing DNS
- node unreachable

Symptoms:
- ping failures
- no internet
- no node communication

## Configuration Verified

Checked interfaces:

ip addr

Checked NetworkManager:

nmcli con show

Checked DNS:

cat /etc/resolv.conf

Internet Validation:

ping -c 4 8.8.8.8

## Host-Only Node Examples

gov-admin:

192.168.56.10

gov-auth:

192.168.56.20

gov-app:

192.168.56.30

## Why It Works
NAT provides outside access.

Host-only adapter provides inter-node communication.

## Outcome
Calidated network stack on all nodes.
