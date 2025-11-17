<p align="center">
  <img src="screenshots/identity_basics_banner.png" alt="Azure AD / Entra ID — Identity Basics Lab Banner" width="100%">
</p>

# 🔐 Project 1 — Microsoft Entra ID Identity Administration Basics  
**Core IAM Foundations — Users • Groups • RBAC • Least Privilege**

![Entra ID](https://img.shields.io/badge/Microsoft_Entra_ID-Identity_Management-blue?style=flat-square)
![RBAC](https://img.shields.io/badge/RBAC-Least_Privilege-blue?style=flat-square)
![Security](https://img.shields.io/badge/Access_Governance-Best_Practices-green?style=flat-square)

---

## 📚 Table of Contents
- [Objective](#objective)
- [Identity Architecture](#identity-architecture)
- [Users Created](#users-created)
- [Groups & Memberships](#groups--memberships)
- [RBAC Role Assignments](#rbac-role-assignments)
- [Least Privilege Justification](#least-privilege-justification)
- [Screenshots](#screenshots)
- [What I Learned](#what-i-learned)
- [Next Project](#next-project)
- [Repo Structure](#repo-structure)

---

## 🎯 Objective
This lab establishes **foundational identity administration skills** inside Microsoft Entra ID (Azure AD):

### ✔️ Created & managed identities  
### ✔️ Implemented role-based access control (RBAC)  
### ✔️ Built security groups with least-privilege design  
### ✔️ Assigned scoped directory roles—*not global roles*  

This project mirrors real enterprise identity governance practices required for modern IAM analyst / admin roles.

---

## 🏗 Identity Architecture

| Component | Naming Standard | Purpose |
|----------|----------------|---------|
| Users | First + Last | Human identities only |
| Groups | `GG-*` | Role-based permissions |
| Roles | Scoped admin | NO global admins granted |
| Admin Separation | YES | Different users hold different admin roles |

---

## 👤 Users Created

| User | Purpose |
|------|---------|
| **Maverick Blaze** | IT Support — user admin duties |
| **Nathan Dash** | Helpdesk — password reset duties |
| **Leah Vanta** | Contractor — no privileged access |
| **Dawsyn Echo** | Contractor — no privileged access |
| **Eddie Spark** | Contractor — no privileged access |

---

## 👥 Groups & Memberships

| Group | Members | Purpose |
|-------|---------|---------|
| `GG-Support-Agents` | Maverick, Nathan | Internal helpdesk team |
| `GG-Contractors` | Leah, Dawsyn, Eddie | Restricted access pool |

---

## 🔐 RBAC Role Assignments

| User | Role Assigned | Reason |
|------|--------------|--------|
| **Maverick Blaze** | **User Administrator** | Needs to create/modify users |
| **Nathan Dash** | **Password Administrator** | Handles only password resets |
| **Contractor Accounts** | **None** | Enforced least privilege |

---

## 🛡 Least Privilege Justification

### ✔ Segregation of Duties
No single user can modify identities **and** reset passwords  
➡️ Prevents abuse & reduces breach blast radius

### ✔ Contractors Receive Zero Administrative Rights
Because contractors often:
- Work temporarily
- Operate outside governance controls
- Pose higher insider risk

### ✔ RBAC Instead of Global Admin
Enterprise security frameworks **require** limited privilege:

> *“If a user doesn’t need it, they shouldn’t have it.”*

---

## 📸 Screenshots

<details>
<summary><strong>👤 Users</strong></summary>

📁 screenshots/
│── users-list.png

css
Copy code

</details>

<details>
<summary><strong>👥 Groups</strong></summary>

📁 screenshots/
│── groups-list.png
│── support-agents-members.png
│── contractors-members.png

css
Copy code

</details>

<details>
<summary><strong>🛡 Role Assignments</strong></summary>

📁 screenshots/
│── mav-user-admin.png
│── nate-password-admin.png

yaml
Copy code

</details>

---

## 🧠 What I Learned

- How Microsoft Entra ID structures identities, groups, and directory roles  
- Why RBAC is mandatory in real-world IAM programs  
- How to enforce **Segregation of Duties (SoD)** for identity safety  
- How to document IAM decisions for audit + compliance evidence  
- That **access governance > technical access** — justification matters

---

## ▶️ Next Project

**Project 2 — MFA Enforcement Lab**  
➡ Enforce Microsoft Authenticator MFA using Authentication Method Policies  
➡ Includes registration campaign + enforcement logic  
🔗 https://github.com/CoachKosik/azure-ad-mfa-enforcement

---

## 📂 Repo Structure

Azure-AD-Entra-ID-Identity-Basics-Lab/
│ README.md
└── screenshots/
    ├─ identity_basics_banner.png
    ├─ users-list.png
    ├─ groups-list.png
    ├─ support-agents-members.png
    ├─ contractors-members.png
    ├─ mav-user-admin.png
    ├─ nate-password-admin.png
