# Day 12 Troubleshooting

## Problem
Nodes could not resolve each other.

## Diagnostics

'''bash

cat /etc/hosts
ping gov-auth

'''

## Root Cause
Missing host resolution

## Fix
Added host mappings to /etc/hosts.

## Verification

'''bash

ping gov-admin

ping gov-auth

ping gov-app

'''
