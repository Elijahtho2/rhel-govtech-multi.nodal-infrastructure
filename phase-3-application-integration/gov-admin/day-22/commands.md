# Day 21 Commands


## Manual (gov-app)


semanage fcontext -a -t httpd_sys_content_t "/webdata(/.*)?"

restorecon -Rv /webdata


## Ansible Playbook


vim ansible/playbooks/selinux_context.yml

'''



'''

- hosts: gov-app
  become: yes
  tasks:

    - name: Set SELinux context

      command: semanage fcontext -a -t httpd_sys_content_t "/webdata(/.*)?"



    - name: Apply context
      command: restorecon -Rv /webdata

'''



Run:


'''bash

ansible-playbook -i ansible/inventory ansible/playbooks/selinux_context.yml

'''

