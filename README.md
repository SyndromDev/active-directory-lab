# active-directory-lab
## Overview
This project demonstrates the deployment and configuration of a basic Active Directory environment using Windows Server.

The goal was to simulate a small company infrastructure with domain services, DNS, and user organization.

## Environment
- Windows Server (Domain Controller)
- VirtualBox/VMware
- Windows 11

## Domain Information
- Domain Name: **company.local**
- Domain Controller: **DC-01**

## Configured Components

### Active directory
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
- Created domain usesr accounts

## Verification 

Dns resolution test:
 - nslookup company.local

Expected result:
 - Returns IP address of Domain Cotroller

## Screenshots

### Active Directory Structure
![AD Structure]
