# Suspicious Activity

## Description
Detects possible malicious PowerShell activity by looking for executed PowerShell scripts

## MITRE ATT&CK Mapping
- Technique: T1059.001 – PowerShell

## Data Source
- Windows Security Event Logs
- Event ID: 4104 (PowerShell Scripts)

## SPL Query
index=* EventCode=4104

## Alert Logic
- Trigger Condition: More than 0 scripts within 5 minutes
- Alert type: Scheduled (runs every five minutes) 
