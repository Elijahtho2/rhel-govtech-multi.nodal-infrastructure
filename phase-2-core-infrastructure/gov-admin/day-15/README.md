# Day 15 - Firewalld

## Commands Practiced
- firewalld
- firewall-cmd


Started:


systemctl enable --now firewalld


Checked:


firewall-cmd --state

firewall-cmd --list-all


Opened HTTP:


firewall-cmd --permanent --add-service=http


Reloaded:


firewall-cmd --reload


## Validation
Verified allowed service list.

## Why It Works
Firewalld controls host-level network policy.

## Multi-Node Reality
Connectivity now depends on policy, not just routing.

## Outcome
Firewall managed and validated.
