# Lab 01 - Azure Network Foundation

## Objective

Build the initial Azure network for the UTS Student Portal.

## Components Created

- Resource Group
- Virtual Network
- Four Subnets

## Design Decisions

- Web servers isolated from application servers.
- Database placed in its own subnet.
- Management subnet reserved for Azure Bastion and administration.
- Used private address space 10.0.0.0/16 for future scalability.

## Lessons Learned

- Azure VNets are the foundation of all Azure networking.
- Subnets separate workloads by function.
