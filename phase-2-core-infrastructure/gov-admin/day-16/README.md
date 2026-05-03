# Day 16 - Apache HTTP Server

## Objective
Install and configure Apache HTTP server on gov-app and validate access from other nodes.

## Machines Used
- gov-app (server)
- gov-admin (client)
- gov-auth (client)


## Commands Practiced
- dnf install
- systemctl 
- firewall-cmd
- curl


## Broken State Introduced
HTTP service not installed or not accessible remotely.


Symptoms:
- curl fails from other nodes
- no web service responding


## Configuration Performed

Installed Apache:


dnf install -y httpd


Enabled service:


systemctl enable --now httpd


Created test page:


echo "GovTech Apache Server - gov-app" > /var/wwww/html/index.html


Opened firewall:


firewall-cmd --permanent --add-service=http

firewall-cmd --reload


## Validation


From gov-admin:


curl http://gov-app


## Why It Works
Apache serves content on port 80.

Firewall allows inbound HTTP traffic.


## Multi-Node Reality
Service hosted on gov-app is consumed by gov-admin and gov-auth.


## Outcome
HTTP service successfully deployed and accessible across nodes.


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

