# Day 01 Summary - Users, Groups, Shared Access

## Overview

Established foundational identity and access control across a multi-node environment by configuring users, groups, and a shared directory with controlled permissions.

## Gov-Admin

- Created users: user100-user500
- Created groups: Alpha, Beta
- Assigned users to appropriate groups
- Configured /sharedgroup directory
- Applied SGID to enforce group inheritance

## Gov-Auth

- Validated group membership behavior
- Successfully accessed shared directory as authorized user (user200)
- Created test file confirming permissions

## Gov-App

- Attempted access with unauthorized user (user400)
- Verified access restriction worked as intended

## Key Outcome

Successfully implemented a controlled shared access model, demonstrating corrrect use of:

- group-based permissions
- SGID behavior
- corss-node validation

## Skills Demonstrated 

- user and group management 
- Linux permissions model
- multi-node validation workflow
- access control troubleshooting
