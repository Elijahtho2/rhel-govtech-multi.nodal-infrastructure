# Day 12 - Host Communication

## Objective 
Establish node-to-node communication using hosts file resolution.

## Commands Practiced 
- ping
- hostname
- cat /etc/hosts

Configured:

192.168.56.10 gov-admin

192.168.56.20 gov-auth

192.168.56.30 gov-app

## Validation

ping gov-admin

ping gov-auth

ping gov-app

## Why It Works
/etc/hosts provides local hostname resolution

## Multi-Node Reality
Nodes now intentionally aware of each other. 

## Outcome
Verified inter-node reachability.
