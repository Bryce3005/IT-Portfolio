# Account Lockout

## 📌 Description
Detects account lockouts by looking for a single user account that has been locked out

## 🧠 MITRE ATT&CK Mapping
- Technique: T1110 – Brute Force

## 📊 Data Source
- Windows Security Event Logs
- Event ID: 4740 (Account Lockout)

## 🔍 SPL Query
index=* EventCode=4740

## 🚨 Alert Logic
- Trigger Condition: More than 0 account lockouts within 5 minutes
- Alert type: Scheduled (runs every five minutes) 
