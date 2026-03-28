# Impossible Travel

## 📌 Description
Detects when a single user is logged in from multiple IP addresses

## 🧠 MITRE ATT&CK Mapping
- Technique: T1078 – Valid Accounts

## 📊 Data Source
- Windows Security Event Logs
- Event ID: 4624 (Successful Logon)

## 🔍 SPL Query
index=* EventCode=4624
| stats dc(src_ip) as ip_count by Account_Name
| where ip_count > 2

## 🚨 Alert Logic
- Trigger Condition: More than 0 user accounts accessed from more than 2 IPs within 5 minutes
- Alert type: Scheduled (runs every five minutes) 
