# Day 10 Commands

## Create Data

'''bash

mkdir archive-lab

echo "test1" > archive-lab/file1.txt

echo "test2" > archive-lab/file2.txt

'''

## Archive

'''bash

tar -cvf arvhive-lab.tar archive-lab

'''

## Compress

'''bash

gzip archive-lab.tar

'''

## Extract

'''bash

mkdir restore-test

tar -xvzf archive-lab.tar.gz -C restore-test

## Verify 

'''bash

ls restore-test/archive-lab
