# Day 1 - Users & Groups Administration

## Objective

- Create users and groups 
- Set permissions for /sharedgroup

## Broken / Issue

- Users missing 
- Groups missing
- Permissions incorrect

![Broken State](..//phase-1-foundation/gov-auth/screenshots/day1-user-broken.png)

## Fix:

- Created users, added to groups
- Set permissions for /sharedgroup

### Commands:

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

![Fixed State](../phase-1-foundation/gov-auth/screenshots/day1-user-fixed.png)

id user100

ls -ld /sharedgroup

su - user100

cd /sharedgroup

touch testfile.txt

ls

![Fixed State](../phase-1-foundation/gov-auth/screenshots/day1-user-fixed.png)


## Screenshots

- Broken State - permission denied

![Broken State](..//phase-1-foundation/gov-auth/screenshots/day1-user-broken.png)

- Fixed State - users & groups created

![Fixed State](../phase-1-foundation/gov-auth/screenshots/day1-user-verification.png)

- Fixed State - permission granted

![Fixed State](../phase-1-foundation/gov-auth/screenshots/day1-user-fixed.png)

