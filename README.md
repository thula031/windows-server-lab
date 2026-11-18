# Windows Server 2019 Home Lab

A Windows Server 2019 home lab built using Oracle VirtualBox to practise Windows Server administration and IT support tasks.

## Overview

This project simulates a small business network environment using a Windows Server 2019 domain controller and a Windows client machine.

The lab covers server configuration, user and group management, network services, access control and shared folder administration.

## Lab Environment

| Component | Configuration |
|---|---|
| Server | Windows Server 2019 |
| Domain Controller | DC001 |
| Client Machine | PC001 |
| Domain | lab.local |
| Virtualisation | Oracle VirtualBox |

## Technologies and Services

- Active Directory Domain Services (AD DS)
- Domain User and Group Management
- Domain Name System (DNS)
- Dynamic Host Configuration Protocol (DHCP)
- Group Policy Objects (GPO)
- File Server and Shared Folder Permissions
- Network Configuration
- Remote Desktop Protocol (RDP) – pending completion

## Repository Structure

```text
windows-server-lab/
│
├── documentation/
│   ├── 01-network-configuration.md
│   ├── 02-active-directory.md
│   ├── 03-dns-configuration.md
│   ├── 04-dhcp-configuration.md
│   ├── 05-group-policy.md
│   ├── 06-file-server.md
│   ├── 07-remote-desktop.md
│   └── 08-troubleshooting.md
│
├── screenshots/
│
├── LAB-NOTES.md
└── README.md
```

## Documentation

Detailed configuration steps, troubleshooting records and practical notes are available in the [documentation folder](documentation/).

The [LAB-NOTES.md](LAB-NOTES.md) file provides an overview of the work completed.

## Project Objective

The purpose of this project is to develop practical experience with Windows Server administration, Active Directory, network services and common IT support responsibilities through a simulated business environment.
