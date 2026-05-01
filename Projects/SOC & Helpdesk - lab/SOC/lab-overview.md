# SOC Lab Overview

**Author:** Bryce Falker  
**Last Updated:** 2026-03-28  
**Lab Type:** Security Operations Center  
**Environment:** Virtualized Lab (VirtualBox)

---

## Purpose of This Lab

This lab is intended to emulate real-world attacker behaviors and practice:
- Threat detection
- Log analysis
- Incident response
- MITRE ATT&CK mapping
- SIEM rule creation and tuning

The purpose is to build hands-on experience locating and addressing adversary activity in simulated environment.

---

## Lab Architecture

**Components:**
- **Attacker Machine:** Kali Linux (simulated adversary)
- **Victim Machine:** Windows 10 / Windows Server
- **SIEM:** Splunk 
- **Logging Sources:**  
  - Windows Event Logs  
  - Sysmon  
  - Firewall / Network logs  
 

**Network Layout:**
- Internal network (isolated)
- NAT or host-only networking


---

## Tools Used

- Splunk (log aggregation & analysis)
- Sysmon (endpoint telemetry)
- PowerShell (scripting & attack simulation)

---

## Attack Scenarios Simulated

### 1. Credential Access
- Brute force login attempts  
- Password spraying  
- Detection mapped to:  
  - Technique: T1110.001 – Password Guessing
  - Technique: T1110.003 – Password Spraying

---

### 2. Lateral Movement
- Remote login attempts between machines  
- Use of valid credentials across systems  
- Detection techniques:
  - Log correlation
  - Suspicious authentication patterns  

---

### 3. Execution Techniques
- Malicious PowerShell execution  
- Script obfuscation  
- Mapped to:
  - Technique: T1059.001 – PowerShell  

---

### 4. Persistence 
- Creation of scheduled tasks  
- New user accounts  
- Mapped to:
  - Technique: T1136.002 – Valid Accounts

---

## Data Sources

| Data Source       | Description |
|------------------|------------|
| Windows Event Logs | Authentication, process creation |
| Sysmon           | Detailed endpoint telemetry |
| SIEM (Splunk)    | Centralized log analysis |

---

## Detection Strategy

- Map logs to MITRE ATT&CK techniques
- Build detections using:
  - SPL queries
  - Correlation searches
  - Behavioral analytics
- Focus on:
  - Failed vs successful logins
  - Anomalous IP behavior
  - Suspicious process execution

---

## Key Detection Goals

- Identify brute force attempts early  
- Detect impossible travel scenarios  
- Monitor suspicious PowerShell activity  
- Correlate endpoint + network events  
- Reduce false positives through tuning  

---

