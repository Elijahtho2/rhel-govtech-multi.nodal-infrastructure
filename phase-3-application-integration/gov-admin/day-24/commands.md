# Day 24 Commands

vim ansible/playbooks/apache_port.yml

'''


'''yaml

- hosts: yes

  tasks:

    - name: Configure Apache port

      lineinfile:
        path: /etc/httpd/conf/httpd.conf

        regexp: '^Listen'

        line: 'Listen 8080;


    - name: Allow SELinux port

      command: semanage port -a -t http_port_t -p tcp 8080


    - name: Open firewall

      command: firewall-cmd --permanent --add-port=8080/tcp


    - name: Reload firewall

      command: firewall-cmd --reload


    - name: Restart Apache

      service:

        name: httpd

        state: restarted

'''


Run:


'''

ansible-playbook -i ansible/inventory ansible/playbooks/apache_port.yml

'''
