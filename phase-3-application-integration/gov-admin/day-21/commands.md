# Day 21 Commands

## Manual (all nodes)

getenforce

sestatus


setenforce 0

getenforce


setenforce 1

getenforce


## Ansible (gov-admin)

ansible all -i ansible/inventory -m command -a "getenforce"
