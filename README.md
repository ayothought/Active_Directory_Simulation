# Active_Directory_Simulation
This project demonstrates the deployment of a **Windows Server Domain Controller (Active Directory)** for a simulated organization, **TUNRAYOTEC.AI**. It covers domain setup, client integration, OU structuring, Group Policy implementation, and access control in an enterprise-like environment.
## 🏢 Company Structure

**TUNRAYOTEC.AI** is modeled as a small IT services firm with the following setup:

- 1 × Windows Server (Domain Controller)
- 1 × Windows 8 Client PC (Sales Department)

---

## 🎯 Project Objectives

- Configure an Active Directory Domain Controller
- Join client machines to the domain
- Design Organizational Units (OUs)
- Implement Group Policies (GPOs)
- Simulate centralized identity and access management

---

## 🌐 Network Design

```
Internet
   ↓
Router (Gateway: 10.0.5.1)
   ↓
Switch
 ┌──────┬
 │      │             
Server  PC1 (Win 8)
```

| Device           | IP Address | Role                          |
|------------------|------------|-------------------------------|
| Windows Server   | 192.168.1.122  | Domain Controller (AD DS) |
| Windows 8 PC     | 192.168.1.184  | Client (Sales Department) |


---

## 🖥️ Domain Configuration

- **Domain Name:** `TUNRAYOTEC.AI`
- **Server Name:** `My Windows`
- **IP Address:** `192.168.1.122` (Static)
- **Roles Installed:**
  - Active Directory Domain Services (AD DS)
  - DNS
  - DHCP

---

## 🗂️ Organizational Units (OUs)

Structured using **Active Directory Users and Computers (ADUC):**

```
TUNRAYOTEC.AI
├── OU: Sales 
│   ├── ABIFOL.SALES
│   
│
├── OU: Marketing
│   └── JAMES.MARKETING
```

---

## 🔐 Group Policy (GPO)

Configured via **Group Policy Management Console:**

- **GPO Name:** `MARKETING DEFAULT POLICY`
- **Linked To:** MARKETING OU
- **Policy Path:**
  ```
  Computer Configuration → Administrative Templates → System → Remove Run from the Start Menu 
  ```
- **Setting:**
  - ** Remove Run from the Start Menu→ Enabled**
  - **Outcome:**  
 Windows cannot find 'Run' within the targeted OU.

---

## 📸 Screenshots

- [Active Directory Domain Structure]()
- [GPO Configuration Screenshot]()
- [Client Joined to Domain]()
- [USB Access Denied Result]()



---

## 🧠 Key Takeaways

- Hands-on experience deploying and managing Active Directory
- Implementation of centralized access control using GPOs
- Practical OU design aligned with organizational structure
- Real-world application of Identity and Access Management (IAM)

---

## 👤 Author

**Motun Ade**  
Cybersecurity Analyst

