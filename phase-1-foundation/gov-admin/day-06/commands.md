# Day 06 Commands

## Create Broken State

'''bash

sleep 500

'''

## Verify Broken State

'''bash

ps aux | grep sleep

pidof sleep

ps -fp $(pidof sleep)

'''

## Fix

'''bash

kill $(pidof sleep)

'''

## Verify Fix

'''bash

ps aux | grep sleep

'''

## Resource Checks

'''bash

top

uptime

free -h

df -h

'''

## Nice Value Example

'''bash

nice -n 10 sleep 500 &

ps -el | grep sleep

killall sleep

'''
