# Day 23 Commands


## Break

chco -t user_home_t /webdata/index.html


## Diagnose

ausearch -m AVC -ts recent


## Ansible Fix

vim ansible/playbook/selinux_fix.yml

'''


'''yaml

- hosts: gov-app

  become: yes
  
  tasks: 

    - name: Restore SELinux context

      command: restorecon -Rv /webdata

'''


Run:


'''bash

ansible-playbook -i ansible/inventory ansible/playbooks/selinux_fix.yml
   
