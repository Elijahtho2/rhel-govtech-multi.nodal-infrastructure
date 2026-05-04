# Day 26 Troubleshooting

## Problem
Cron job executing.

## Diagnostics

crontab -l

journalctl

## Root Cause
Cron entry missing or incorrect syntx.


## Fix
Re-added cron job.


## Verification


journalctl | grep GovTech
