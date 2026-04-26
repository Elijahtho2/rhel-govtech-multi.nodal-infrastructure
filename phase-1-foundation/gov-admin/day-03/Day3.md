# Day 3 - Shared Directory (SGID)
VM: Gov-Auth

## Objectives

- Configure shared directory
- Enable SGID
- Validate group inheritance

## Broken

### Commands

mkdir /sharedgroup

chown root:Alpha /sharedgroup

chmod 770 /sharedgroup

## Troubleshoot

### Commands

ls -ld /sharedgroup

#### Test

su - user100

touch /sharedgroup/file1

ls -l /sharedgroup

exit

## Fixed

- Apply SGID

### Commands

chmod 2770 /sharedgroup

## Verification

### Commands

ls -ld /sharedgroup

#### Test

su - user100

touch /sharedgroup/user100-file

ls -l /sharedgroup

exit


su - user200

touch /sharedgroup/user200-file

ls -l /sharedgroup

exit

## Screenshots

Directory Permissions

File Creation showing group inheritance
