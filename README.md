# enterprise-network-infrastructure
Enterprise network infrastructure project built with Cisco Packet Tracer, featuring VLANs, OSPF, centralized DHCP, ACLs, SSH, and Port Security.
# Enterprise Network Infrastructure

A practical enterprise network infrastructure project designed and implemented using **Cisco Packet Tracer**.

## Project Overview

This project simulates a small enterprise network consisting of a **Headquarters (HQ)** and a **Branch Office** connected through a routed WAN.

The network was designed with department-based VLAN segmentation, dynamic routing, centralized DHCP, secure remote management, and access control policies.

## Network Architecture

### Headquarters

* VLAN 10 — HR
* VLAN 20 — Finance
* VLAN 30 — IT
* VLAN 40 — Servers
* VLAN 99 — Management
* Layer 3 Core Switch
* Edge Router
* Centralized DHCP Server

### Branch Office

* VLAN 50 — Sales
* VLAN 60 — Support
* VLAN 99 — Management
* Branch Router
* Access Switch

## Technologies & Features

* VLAN Segmentation
* Inter-VLAN Routing
* OSPF Dynamic Routing
* Centralized DHCP
* DHCP Relay
* Router-on-a-Stick
* SSH Version 2
* Extended ACLs
* Port Security
* Management VLAN
* IPv4 Subnetting
* Cisco IOS Configuration
* Network Troubleshooting & Verification

## Routing

OSPF is implemented between the HQ Core, HQ Edge Router, and Branch Router using **Area 0**.

The routers exchange routes dynamically, allowing communication between the HQ and Branch networks.

## Security

The project includes several basic enterprise security controls:

* SSH for secure remote device management
* Extended ACLs to restrict specific inter-department traffic
* Port Security with sticky MAC addresses
* Dedicated Management VLAN

### Implemented ACL Policies

| Source  | Destination | Result  |
| ------- | ----------- | ------- |
| Sales   | HR          | Blocked |
| Sales   | Server      | Allowed |
| Support | Finance     | Blocked |
| Support | Server      | Allowed |

## DHCP

A centralized DHCP server provides IP configuration for the following networks:

* HR
* Finance
* IT
* Sales
* Support

DHCP relay is configured on the required Layer 3 interfaces.

## Project Evidence

### Network Topology

![Network Topology](Screenshots/Topology.png)

### OSPF Neighbor Verification

![OSPF Neighbor](Screenshots/OSPF-Neighbor.png)

### OSPF Routes

![OSPF Routes](Screenshots/OSPF-Routes.png)

### ACL Verification

![ACL Verification](Screenshots/ACL-Verification.png)

### SSH Verification

![SSH Verification](Screenshots/SSH-Verification.png)

### Port Security Verification

![Port Security](Screenshots/Port-Security-Verification.png)

## Project Files

* `Packet-Tracer/` — Cisco Packet Tracer project
* `Screenshots/` — Configuration and verification screenshots
* `Documentation/` — Detailed project documentation

## Tools

* Cisco Packet Tracer
* Cisco IOS

## Project Status

**Completed and verified**

This project was built as a practical networking portfolio project to demonstrate hands-on implementation of enterprise networking concepts.
