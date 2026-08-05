# UTS Student Portal - Infrastructure Deployment

## Objective

Build a secure three-tier Azure infrastructure for a Student Portal.

---

## Architecture

Internet

↓

Azure Application Gateway (Planned)

↓

Web VM

↓

API VM

↓

SQL VM

Administrative Access

↓

Azure Bastion

---

## Components

Resource Group

VNet

WebSubnet

APISubnet

SQLSubnet

AzureBastionSubnet

Network Security Groups

Azure Bastion

Windows Server 2025 VMs

IIS Web Server

---

## Lessons Learned

- Why private IPs are preferred for backend servers.
- Azure Bastion removes the need for public RDP.
- NSGs filter network traffic but do not authenticate users.
- Three-tier architecture improves security and scalability.
