# Added to Admin Group

## 📌 Description
Detects possible privilege escalation by looking for users added to admin group in a short time span

## 🧠 MITRE ATT&CK Mapping
- Technique: T1098 – Account Manipulation

## 📊 Data Source
- Windows Security Event Logs
- Event ID: 4728 (Added to security local group) and 4732 (Added to security global group)

## 🔍 SPL Query
index=* EventCode=4728 OR EventCode=4732

## 🚨 Alert Logic
- Trigger Condition: More than 0 users added to the admin group within 5 minutes
- Alert type: Scheduled (runs every five minutes) 
