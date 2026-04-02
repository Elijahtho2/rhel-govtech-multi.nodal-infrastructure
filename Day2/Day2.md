# Day 2 - Sudo Access 

## Objective
- Grant sudo access to user200
- Validate sudo access

# Broken State
su - user200
sudo systemctl restart sshd
![Broken State](../screenshots/phase-1-auth/day2-sudo-broken.png)

# Fix
su -
usermod -aG wheel user200
visudo
[ensure]    %wheel ALL=(ALL) ALL
![Fixed State](../screenshots/phase-1-auth/day2-sudo-fixed.png)

# Verification
su - user200
sudo systemctl restart sshd
![Verified](../screenshots/phase-1-auth/day2-sudo-verified.png)

## Screenshots
![Broken State](../screenshots/phase-1-auth/day2-sudo-broken.png)
![Fixed State](../screenshots/phase-1-auth/day2-sudo-fixed.png)
![Verified](../screenshots/phase-1-auth/day2-sudo-verified.png)




