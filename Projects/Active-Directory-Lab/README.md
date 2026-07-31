# Active Directory Home Lab

## Overview

I built this lab to get experience with Windows Server and Active Directory.

The goal was to learn how to install and configure Active Directory, create users and groups, organize Organizational Units, work with Group Policy, and practice common help desk tasks in a business environment.

---

## Note

I'm still learning Windows Server, Active Directory, and GitHub, so I used Microsoft documentation and YouTube tutorials while building this lab. I also used this project to practice writing better documentation for my GitHub portfolio.

I've included the resources I used at the bottom of this README.

---

# Environment

| Component | Details |
|-----------|---------|
| Hypervisor | Oracle VirtualBox |
| Operating System | Windows Server 2025 Evaluation |
| Server Name | DC01 |
| Domain | homelab.local |
| Active Directory | Active Directory Domain Services (AD DS) |
| DNS | Installed with Active Directory |

---

# Skills Demonstrated

- Windows Server
- Active Directory
- DNS
- Static IP Configuration
- Domain Controller Deployment
- Organizational Units (OUs)
- User & Group Management
- Security Groups
- Group Policy
- Basic Help Desk Tasks

---

# Lab Walkthrough

## 1. Configure the Server

- Installed Windows Server 2025
- Renamed the server to DC01
- Configured a static IP address
- Verified network connectivity with `ipconfig` and `ping`

![Server Renamed](screenshots/01-server-renamed-dc01.png)

![Static IP Verification](screenshots/02-static-ip-verification.png)

---

## 2. Install Active Directory

Installed the Active Directory Domain Services role.

![Install AD DS](screenshots/03-add-active-directory.png)

![AD DS Installed](screenshots/04-ad-ds-installed.png)

---

## 3. Promote the Server

Created a new Active Directory forest using:

**homelab.local**

A DNS delegation warning appeared during setup, which is expected when creating a new forest.

All prerequisite checks passed before promoting the server.

![DNS Delegation Warning](screenshots/05-dns-delegation-warning.png)

![Prerequisites Check](screenshots/06-prerequisites-check.png)

![Domain Controller Online](screenshots/07-domain-controller-online.png)

---

## 4. Create Organizational Units

Created Organizational Units for different departments and resources.

Created:

- Company Users
- HR
- IT
- Servers
- Workstations
- Security Groups
- Disabled Users

![Organizational Units](screenshots/08-organizational-units.png)

---

## 5. Create Users

Created users for different departments.

![Company Users](screenshots/09-company-users-created.png)

![IT Users](screenshots/10-it-users-created.png)

![HR Users](screenshots/11-hr-user-created.png)

---

## 6. Create Security Groups

Created security groups and added users to the correct groups.

Groups created:

- Company Employees
- HR Staff
- IT Support
- Domain Admins (Labs)

![Security Groups](screenshots/12-security-groups-created.png)

![Group Membership](screenshots/13-group-membership.png)

---

## 7. Active Directory Administration

Completed a few common Active Directory administration tasks.

### Disable a User

Disabled a user account.

![Disabled Account](screenshots/14-disabled-account.png)

### Move a User

Moved a user to the HR OU and updated group membership.

![User Moved to HR](screenshots/15-user-moved-to-hr.png)

![Updated Group Membership](screenshots/16-group-membership-updated.png)

---

## 8. Configure Group Policy

Created a Group Policy Object named **Company Desktop Policy**.

Linked it to the Company Users OU and blocked access to Control Panel and Windows Settings.

![Company Desktop Policy](screenshots/17-company-desktop-policy-created.png)

![Linked GPO](screenshots/18-gpo-linked-to-company-users.png)

![Control Panel Policy Enabled](screenshots/19-control-panel-policy-enabled.png)

---

## 9. Help Desk Scenarios

### New Employee

Created a new HR employee and assigned the correct Organizational Unit and security group.

![New User Onboarding](screenshots/20-new-user-onboarding.png)

### Employee Offboarding

Disabled a user account and moved it into the Disabled Users OU.

![Disabled User](screenshots/21-disabled-user.png)

---

# What I Learned

This was my first time building an Active Directory environment from scratch.

By the end of this project I was comfortable:

- Installing Active Directory
- Promoting a Domain Controller
- Creating Organizational Units
- Managing users and security groups
- Creating and linking Group Policy Objects
- Performing common Active Directory administration tasks

I also became more comfortable navigating Windows Server and documenting my work as I completed the lab.

---

# Learning Resources

I used a mix of Microsoft documentation and community tutorials while building this lab. I also watched a few GitHub videos while learning how to better organize and document my projects.

## Microsoft Learn

- [Windows Server Documentation](https://learn.microsoft.com/windows-server/)
- [Active Directory Domain Services Overview](https://learn.microsoft.com/windows-server/identity/ad-ds/get-started/active-directory-domain-services-overview)

## Active Directory

- [Active Directory Home Lab Playlist](https://youtu.be/fbfSKgV2in8?si=hfXU7kx2C0gcxSO7)

## GitHub & Documentation

- [GitHub Portfolio Tutorial](https://youtu.be/z8UPAVTh2aE?si=U-vHv2dFYEV1Yp8p)
- [GitHub README Tutorial](https://youtu.be/zgqfWLHNKLk?si=wgqzEjhG6_o13NBN)
- [Markdown & GitHub README Guide](https://youtu.be/AU2I-GvQc0Q?si=cba-fo7aufMMFC1k)
- [GitHub README Tutorial (Additional)](https://youtu.be/gbBwIPs1NPw?si=GXLA4mZjFOluXmux)
- [GitHub Profile & Repository Tips](https://youtu.be/OShHVX_dBjo?si=_O0IbAha4nsfiRZ_)

---

# Next Steps

Some things I'd like to add to this lab in the future:

- Join a Windows client to the domain
- Create more Group Policy Objects
- Configure shared folders and NTFS permissions
- Learn basic Active Directory PowerShell commands
- Expand the lab with additional Windows clients and servers

