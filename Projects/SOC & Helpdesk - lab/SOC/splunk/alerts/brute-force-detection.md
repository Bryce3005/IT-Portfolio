# Brute Force Detection

## Description
Detects possible brute force attacks by looking for multiple failed logins from a single account in a short time span

## MITRE ATT&CK Mapping
- Technique: T1110 – Brute Force

## Data Source
- Windows Security Event Logs
- Event ID: 4625 (Failed Logon)

## SPL Query
index=* EventCode=4625 | stats count by Account_Name
| where count > 4

## Alert Logic
- Trigger Condition: More than 4 failed login attempts within 5 minutes
- Alert type: Scheduled (runs every five minutes) 
