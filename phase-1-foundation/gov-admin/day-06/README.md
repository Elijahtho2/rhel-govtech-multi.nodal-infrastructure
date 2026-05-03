# Day 06 - Process & System Operations

## Objective
Practice monitoring, identifying, controlling, and troubleshooting Linux processes and system resource usage on gov-admin. 

## Machine Used
gov-admin

## Skills Practiced
- ps
- top
- pidof
- kill
- killall
- nice
- renice
- free -h
- uptime
- df -h

## Broken State Introduced
A background process was intentionally created and left running:

sleep 500 &

Symptoms:
- unecessary process consuming PID
- process visible in ps output
- test process should not remain active

## Troubleshooting Performed
Verified running process:

ps aux | grep sleep

Retrieved process id:

pidof sleep

Confirmed process state:

ps -fp $(pidof sleep)

Terminated process:

kill $(pidof sleep)

Verified process removal:

ps aux | grep sleep

## Why it Works:
Linux manages every running task as a process identified by a PID.

Using ps, pidof and kill allows direct control over system activity.

## Validation Performed
Verified:
- process existed
- process was killed
- process no longer existed

Additional system checks performed:

uptime

free -h

df -h

## Multi-Nodal Reality
This exercise is local to gov-admin

## Outcome
Successfully:
- created broken process condition
- diagnosed process
- terminated process
- validated system health

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
