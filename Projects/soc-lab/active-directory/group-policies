# Group Policy Objects (GPOs)

## 📌 Overview
This lab applies Group Policy Objects (GPOs) to enforce security controls, simplify configurations, and create audit logs from activity on the domain.

Policies are added to Organizational Units (OUs) based on role-based access control and department-specific security requirements.

---

## 🔐 Domain Security Foundation

### 📍 Scope
- Applied at the domain level

### ⚙️ Policies Configured
- Password minimum length: 12 characters
- Password complexity: Enabled
- Account lockout threshold: 5 failed attempts
- Account lockout duration: 15 minutes

### 🎯 Purpose
- Protect against brute force attacks
- Enforce strong password policies

---

## 🔍 Audit & Logging Policy

### 📍 Scope
- Applied to all systems

### ⚙️ Policies Configured
- Audit Logon Events
- Audit Account Logon
- Audit Account Management
- Audit Process Creation
- PowerShell Script Block Logging
- Command-line logging enabled

### 🎯 Purpose
- Provide additional information for SIEM monitoring 
- Support detection of malicious activity

---

## 🛡️ ADMINS OU – Monitoring Policy

### 📍 Scope
- ADMINS OU

### ⚙️ Policies Configured
- PowerShell logging enabled
- Advanced audit policies enabled
- Command-line process logging enabled
- Optional: USB storage blocked

### 🎯 Purpose
- Monitor high-privilege accounts tightly
- Detect misuse of administrative tools

---

## 💼 EXECUTIVES OU – Restricted Environment

### 📍 Scope
- Executives OU

### ⚙️ Policies Configured
- Command Prompt disabled
- PowerShell restricted
- Screen lock enforced (5 minutes)
- BitLocker enabled (if supported)
- Software installation restricted

### 🎯 Purpose
- Protect critical users from phishing and attacks
- Decrease attack vectors

---

## 💰 FINANCE OU – Data Protection

### 📍 Scope
- Finance OU

### ⚙️ Policies Configured
- Removable storage (USB) blocked
- File system auditing enabled
- Restricted file execution

### 🎯 Purpose
- Prevent data exfiltration
- Monitor access to sensitive financial information

---

## 🧑‍💼 HR OU – Privacy Protection

### 📍 Scope
- HR OU

### ⚙️ Policies Configured
- Control Panel access restricted
- System tools disabled (Task Manager, Registry Editor)
- User account management auditing enabled

### 🎯 Purpose
- Protect personally identifiable information (PII)
- Monitor account-related changes

---

## 🛠️ IT OU – Flexible but Monitored

### 📍 Scope
- IT OU

### ⚙️ Policies Configured
- PowerShell and CMD allowed
- Advanced audit logging enabled
- Restricted administrative privileges where needed

### 🎯 Purpose
- Allow operational flexibility
- Maintain view of administrative actions

---

## 📢 MARKETING OU – Controlled Internet Use

### 📍 Scope
- Marketing OU

### ⚙️ Policies Configured
- Executable restrictions from Downloads folder
- Browser security features enabled

### 🎯 Purpose
- Reduce risk from web-based threats
- Limit execution of untrusted files

---

## ⚙️ OPERATIONS OU – Stability Focus

### 📍 Scope
- Operations OU

### ⚙️ Policies Configured
- Software installation restricted
- Unnecessary services disabled
- Strong authentication policies enforced

### 🎯 Purpose
- Uphold system stability
- Reduce unauthorized changes

---

## 💼 SALES OU – Remote Security

### 📍 Scope
- Sales OU

### ⚙️ Policies Configured
- Screen lock enforced (short timeout)
- Local administrator rights restricted
- VPN requirement (conceptual)

### 🎯 Purpose
- Secure remote users
- Reduce risk from unmanaged environments

---

## 🔗 GPO Management

- GPOs are linked to their proper OUs using Group Policy Management Console
- Policies are applied using `gpupdate /force` for testing and validation

---

## 📸 Screenshots
*(Insert screenshots of GPMC, applied GPOs, and policy settings)*

---

## 🧾 Notes
These Group Policy applications simulate enterprise-level security controls and provide the adequate logging and restrictions to aid in SOC monitoring and incident response.
