# Day 10 Troubleshooting

## Problem
Need backup archive and recovery test.

## Diagnostics

'''bash

ls 

tar -tvf archive-lab.tar.gz

'''

## Root Cause
Files not packaged or compressed.

## Fix

'''bash

rar -cvf archive-lab.tar archive-lab

gzip archive-lab.tar

tar -xvzf-lab.tar.gz -C restore-test

'''

## Verification

'''bash

ls restore-test/archive-lab

'''

Archive restore successfully.
