# Day 25 Commands

vim ansible/playbooks/user_policy.yml

'''


'''yaml

- hosts: gov-auth

  become: yes

  tasks:

    - name: Create user

      user:

        name: contractor1

        state: present


    - name: Set password aging

      command: chage -M contractor1

'''


Run: 


'''bash

ansible-playbook -i ansible/inventory ansible/playbooks/user_policy.yml
