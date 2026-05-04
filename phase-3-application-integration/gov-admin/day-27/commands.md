# Day 27 Commands


mkdir -p ~/scripts

vim ~/scripts/check-system.sh

'''


'''bash

#!/bin/bash


echo "Hostname:"

hostname


echo "Disk Usage:"

df -h


echo "Memory:"

free -h

'''


'''bash

chmod +x ~/scripts/check-system.sh

./scripts/check-system.sh

'''
