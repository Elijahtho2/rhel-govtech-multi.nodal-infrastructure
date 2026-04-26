# Day 06 Troubleshooting

## Problem
Test process remained running.

## Symptoms
Command:

ps aux | grep sleep

Returned:

sleep 500

## Root Cause
Background process intentionally launched and not stopped.

## Diagnostic Commands

'''bash

pidof sleep

ps -fp $(pidof sleep)

'''

## Corrective Action 

'''bash

kill $(pidof sleep)

'''

## Verification

'''bash

ps aux | grep sleep

'''

No Active sleep process remained.

## Lessons Learned
- identify processes
- isolate by PID
- terminate safely
- verify fixes
