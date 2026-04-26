# Day 1 - Users & Groups Administration

## Objective

- Create users: user100-user500
- Create groups: Alpha, Beta
- Assubg users to groups
- Create /sharedgroup directory 
- Set permissions for /sharedgroup

## Broken / Issue

- user100 cannot access /sharedgroup
- user400 incorrectly placed in Alpha
- Users missing 
- Groups missing
- Permissions incorrect

![Broken State](../screenshots/day1-user-broken.png)

## Troubleshoot

### Commands:

id user100

groups user400

ls -ld /sharedgroup

## Root-Cause

- Incorrect group membeership and missing directory group ownership alignment

## Fixed:


### Commands:

usermod -aG Alpha user200

usermod -G Beta user400

chown :Alpha /sharedgroup

chmod 770 /sharedgroup

## Why-It-Works

- Linux access is determined by UID/GID mapping
- Group ownership + permissions define shared access boundaries

## System-Impact

- Identity management controls access to All services and files
- Misconfigured groups cascade into permission failures system-wide

## Cross-Node Insight

- Users/groups exist only on gov-admin unless created on other VMs
1. Created Users:

useradd user100

useradd user200

useradd user300

useradd user400

useradd user500

2. Created group:

groupadd Alpha
groupadd Beta

3. Added users to groups:

usermod -aG Alpha user100

usermod -aG Alpha user200

usermod -aG Alpha user300

usermod -aG Beta user400

usermod -aG Beta user500

4. Created shared directory and set permissions:

mkdir /sharedgroup

chown :Alpha /sharedgroup

chmod 2770 /sharedgroup

## Verifcation

### Commands:

getent groups | grep "users"||"Alpha"||"Beta"

![Fixed State](../screenshots/day1-user-verification.png)

id user100

ls -ld /sharedgroup

su - user100

cd /sharedgroup

touch testfile.txt

ls

![Fixed State](../screenshots/day1-user-fixed.png)


## Screenshots

- Broken State - permission denied

![Broken State](../screenshots/day1-user-broken.png)

- Fixed State - users & groups created

![Fixed State](../screenshots/day1-user-verification.png)

- Fixed State - permission granted

![Fixed State](../screenshots/day1-user-fixed.png)

