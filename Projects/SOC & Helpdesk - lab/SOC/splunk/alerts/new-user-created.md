# New User Created

## Description
Detects new users by looking at newly created accounts in a short time span

## MITRE ATT&CK Mapping
- Technique: T1136 – Create Account

## Data Source
- Windows Security Event Logs
- Event ID: 4720 (New user account)

## SPL Query
index=* EventCode=4720

## Alert Logic
- Trigger Condition: More than 0 created users within 5 minutes
- Alert type: Scheduled (runs every five minutes) 
