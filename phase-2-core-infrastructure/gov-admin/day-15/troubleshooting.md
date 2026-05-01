# Day 15 Troubleshooting

## Problem
Service access blocked

## Diagnostics

'''bash

firewall-cmd --list-all

'''


## Root Cause
HTTP service absent from allowed services.

### Fix

'''bash

firewall-cmd --permanent --add-service=http

firewall-cmd --reload

'''


## Verification

'''bash

firewall-cmd --list-all

'''
