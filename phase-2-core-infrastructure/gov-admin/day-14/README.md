# Day 14 - Multi-Node SSH Trust

## Objective
Configure passwordless SSH trust

## Commands Practiced
- ssh-keygen
- ssh-copy-id


Generated key:


ssh-keygen


Copied trust:


ssh-copy-id gov-auth

ssh-copy-id gov-app


Validated:


ssh gov-auth hostname
ssh-gov-app hostname

## Why It Works
Public key copied to authorized_keys enables passwordless trust.

## Outcome
SSH trust established.
