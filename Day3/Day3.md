# Day 3 - SSH Service & SELinux Check

## Objectives:

- Enable SSH service
- Temporarily disable SELinux
- Verify SSH Login

## Broken 

- SSHD stopped
- SELinux enforcing
- SSH login fails

### Commands:

sudo systemctl stop sshd
ssh user200@localhost
getenforce

![Broken State](../screenshots/phase-1-auth/day3-SSH-broken.png)

## Fix

- SSH enabled and running
- SELinux permissive
- SSH login succeeds

### Commands:

sudo systemctl enable --now sshd
sudo setenforce 0

![Fixed State](../screenshots/phase-1-auth/day3-SSH-fixed.png)

## Verification

### Commands:

ssh user200@gov-auth

![Verified](../screenshots/phase-1-auth/day3-SSH-verified.png)

## Screenshots

![Broken State](../screenshots/phase-1-auth/day3-SSH-broken.png)

![Fixed State](../screenshots/phase-1-auth/day3-SSH-fixed.png)

![Verified](../screenshots/phase-1-auth/day3-SSH-verified.png)

