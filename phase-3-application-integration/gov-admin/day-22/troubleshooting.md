# Day 22 Troubleshooting

## Problem
Apache could not access /webdata.

## Diagnostics


ls -Zd /webdata

curl http://gov-app


## Root Cause
Incorrect SELinux context.


## Fix

restorecon -Rv /webdata


## Verification

curl http://gov-app
