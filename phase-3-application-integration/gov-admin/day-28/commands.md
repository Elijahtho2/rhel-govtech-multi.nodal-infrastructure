# Day 28 Commands

vim ~/scripts/check-nodes.sh

'''



'''bash

#!/bin/bash


for node in gov-admin gov-auth gov-app

do

    ping -c 2 $node &>/dev/null


    if [ $? -eq 0 ]; then

        echo "$node reachable"

    else

        echo "$node unreachable"

    fi

done

'''



'''bash

chmod +x ~/scripts/check-nodes.sh

./scripts/check-nodes.sh

'''



## Run via Ansible


'''bash

ansibleall -i ansible/inventory -m script -a "~/scripts/check-nodes.sh"

'''
