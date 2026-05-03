# Day 21 Troubleshooting

## Problem SELinux enforcement needed validation across nodes.

## Diagnostics

getenforce

se status


## Root Cause
SELinux temporarily set to permissive.


## Fix

setenforce 1


## Verification

ansible all -i ansible/inventory -m command -a "getenforce"
