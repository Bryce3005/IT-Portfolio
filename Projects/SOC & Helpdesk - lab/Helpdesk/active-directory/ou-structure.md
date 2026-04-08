# Organizational Unit (OU) Structure

## 📌 Overview
This Active Directory simulation is designed using Organizational Units (OUs) to reflect a realistic enterprise organizational structure. Each OU represents a department and is used to enforce role-based access control (RBAC) and Group Policy Objects (GPOs).

## 🧱 OU Infrastructure

The domain is seperated into eight different OUs:

- ADMINS
- Executives
- Finance
- HR
- IT
- Marketing
- Operations
- Sales

Each OU includes:
- User accounts
- Security groups
- Department-specific policies

## 🧠 Design Purpose

- Separate users by department
- Apply specific security rules using GPOs
- Support least privilege access control
- Simplify administration and policy enforcement

## 🔐 Security Groups

Each OU includes security groups used for:
- Role-based access control (RBAC)
- Permission assignment to resources
- Handling administrative privileges

There are 18 security groups within this lab:
- Global Groups
  - GG_SysAdmins
  - GG_SecurityTeam
  - GG_Sales
  - GG_Payroll
  - GG_Operations
  - GG_Marketing
  - GG_Managers
  - GG_IT
  - GG_HR
  - GG_Helpdesk
  - GG_Finance
  - GG_Executives
  - Backup Operators
- Domain Local
  - DL_Public_Read
  - DL_IT_RW
  - DL_HR_RW
  - DL_Finance_RW

## ⚙️ Group Policy Objects

Group Policy Objects (GPOs) are connected to each OU to enforce security policies based on specific department responsibilities.

Policies
- ADMINS: Enhanced logging and monitoring
- Executives: Restricted system access and enforced screen lock
- Finance: File auditing and removable media restrictions
- IT: Advanced logging with fewer restrictions
- Sales: Prohibited access to Control Panel
- HR: Prevent access to registry editing tools

## 🔍 Benefits of OU Structure

- Centralized management of users and policies
- Flexible design for future incorporation of new groups 
- Hardened security through policy segmentation
- Easier troubleshooting and administration

## 🖥️ Hierarchy

FalkerINC.net
│
| ── ADMINS
│   ── Admin Users
│   ── Admin Groups
│
| ── Executives
│   ── Users
│   ── Groups
│
| ── Finance
│   ── Users
│   ── Groups
│   ── Shared Resources
│
| ── HR
│   ── Users
│   ── Groups
│
| ── IT
│   ── Users
│   ── Groups
│   ── Service Accounts
│
| ── Marketing
│   ── Users
│   ── Groups
│
| ── Operations
│   ── Users
│   ── Groups
│
└── Sales
    ── Users
    ── Groups
