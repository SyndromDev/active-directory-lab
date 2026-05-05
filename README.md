# Active Directory Home Lab

##  Overview
This project demonstrates the deployment and configuration of a basic Active Directory environment using Windows Server.

The goal was to simulate a small company infrastructure with domain services, DNS, and user organization.

---

##  Environment
- Windows Server (Domain Controller)
- VirtualBox / VMware
- Windows 11 (Client - optional)

---

##  Domain Information
- Domain Name: **company.local**
- Domain Controller: **DC-01**

---

##  Configured Components

### Active Directory
- Installed Active Directory Domain Services (AD DS)
- Promoted server to Domain Controller

### DNS
- Configured DNS server on DC
- Created Forward Lookup Zone: `company.local`
- Verified domain resolution

### Organizational Structure
- Created OUs:
  - IT
  - HR
  - Users
- Created domain user accounts

---

##  Verification

DNS resolution test:
- nslookup company.local


Expected result:
- Returns IP address of Domain Controller

---

##  Screenshots

### Active Directory Structure
![AD Structure](screenshots/structure.png)

### Users in Organizational Units
![Users](screenshots/ActiveDirectory.png)

### Users in IT (Helpdesk)
![Helpdesk](screenshots/helpdesk.png)

### Users in IT (Admins)
![Admins](screenshots/SysAdmins.png)

### Users in Employees
![Employees](screenshots/Users.png)

### DNS Configuration
![DNS](screenshots/DNSmanager.png)

### Company local
![Company local](screenshots/companylocal.png)

### Domain Resolution Test
![NSLookup](screenshots/Name.png)

### Server-client
![Server-client](screenshots/Server-client.png)

---

##  Notes
Domain join from client machine was not completed due to Windows edition limitations (Home edition).

---

##  Outcome
Successfully deployed a functional Active Directory environment with DNS and organizational structure simulating a real-world company setup.
