# Day 17 Troubleshooting

## Problem
Apache could not serve /webdata.

## Diagnostics

curl http://gov-app

ls -Zd /webdata


## Root Cause
Incorrect SELinux context.


## Fix


seamanage fcontext -a -t httpd_sys_content_t "/webdata(/.*)?"

restorecon -Rv /webdata


## Verification

curl http://gov-app
