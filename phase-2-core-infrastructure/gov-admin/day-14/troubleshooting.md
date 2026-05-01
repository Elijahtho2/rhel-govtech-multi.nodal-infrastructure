# Day 14 Troubleshooting

## Problem
SSH required passwords.

## Root Cause
No authorized_keys trust.

## Fix

'''bash

ssh-copy-id gov-auth

ssh-copy-id gov-app

'''



## Verification

'''bash

ssh-gov-auth hostname

ssh-gov-app hostname

'''


Returned remote hostnames without password prompts.
