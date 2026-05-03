# Day 10 - Archive and File Management

## Objective
Practice tar, gzip, archive create and restoration.

## Machine Used 
gov-admin

## Commands Practiced
- tar 
- gzip
- gunzup
- mkdir
- cp
- ls

## Broken State Introduced
Files existed unarchived.

## Test Data Created

mkdir archive-lab.tar

## Restored Archive

mkdir restore-test

tar -xvzf archive-lab.tar.gz -C restore-test

## Validation

ls archive

ls restore-test

tar -tvf archive-lab.tar.gz

## Why It Works
Tar packages files.

gzip compresses archive.

Extraction restores structure.

## Multi-Node Reality
Archive work local to gov-admin

## Outcome 
Created, compressed and restored archive successfully.


## Automation Opportunity

This task can be automated using Ansible.

Future automation includes:
- remote execution across nodes
- configuration enforcement
- repeatable deployment


## AI Usage 

AI was used to:
- validate commands
- troubleshoot issues
- confirm expected outputs

