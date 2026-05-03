# Day 23 Troubleshooting

## Problem
Apache denied access.


## Diagnostics

ausearch -m AVC -ts recent


ls -Z /webdata/index.html


## Root Cause
Incorrect SELinux context applied.


## Fix

restorecon -Rv /webdata


## Verification

curl http://gov-app
