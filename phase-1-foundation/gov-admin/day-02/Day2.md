# Day 2 - Permissions and Ownership
- VM: Gov-Auth

## Objectives:

- Configure directory ownership
- Apply permissions
- Validate access control

## Broken

### Commands:

mkdir /securedata

chmod 777 /securedata

## Troubleshoot

### Commands

ls -ld /securedata

stat /securedata

#### Test

#### Commands

su - user 400

cd /securedata

## Fixed

### Commands

#### Coorect Ownership

chown root:Alpha /securedata

#### Correct Permissio### Commands

chmod 770 /secure data

## Verification

### Commands

ls -ld /securedata

#### Test

su - user100

cd /securedata

exit

su - user400

cd /secure data

## Screenshots


