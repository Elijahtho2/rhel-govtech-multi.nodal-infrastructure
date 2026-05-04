# Day 25 Troubleshooting

## Problem
User plicy not enforced.


## Diagnostics

chage -l contractor1


## Root Cause
Policy not configured.


## Fix

chage -M 30 contractor1


## Verification

chage -l contractor1
