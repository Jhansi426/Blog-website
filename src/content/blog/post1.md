---
title: "University Network using Cisco Packet Tracer"
description: "Design and simulate a multi-building university campus network with segmented VLANs, high-speed trunks, and centralized services using Cisco Packet Tracer."
pubDate: "Jun 08 2025"
heroImage: "/main.png"
badge: "Campus Netowork"
tags: ["networking", "packet-tracer", "campus-network"]
---

# UNIVERSITY-NETWORK-USING-CISCO-PACKET-TRACER

## 📖 Table of Contents

1. [Project Overview](#project-overview)  
2. [Building-by-Building Breakdown](#building-by-building-breakdown)  
3. [IP Addressing & VLAN Design](#ip-addressing--vlan-design)  
4. [Key Hardware Components](#key-hardware-components)  
5. [Data Flow and Routing](#data-flow-and-routing)  
6. [Images](#images)  
7. [Security & Management](#security--management)  
8. [Benefits & Scalability](#benefits--scalability)  
9. [Getting Started](#getting-started)  

---

## 🚀 Project Overview

This project documents the design and implementation of a **multi-building university campus network** in Cisco Packet Tracer. It connects:

- **Building A:** Management, HR, Finance, Business departments  
- **Building B:** Electronics & Communication (E&C), Art & Design departments  
- **Building C:** Student computer labs, IT services, Web & FTP servers  
- **Smaller Building:** Additional labs and admin workspace  
- **Core Infrastructure:** Central router cluster, multilayer core switch, email server  

Each department or lab is served by its own access switch. Inter-building links use high-speed fiber trunks and routed subinterfaces, providing segmentation, reliability, and centralized management.

---


## 🏢 Building-by-Building Breakdown

### Building A (192.168.1.0/24 – 192.168.4.0/24)
- **Switch-18 (2960-24TT)** uplinks to CoreSW  
  - **Mgmt Dept (VLAN 10):** PC0 (192.168.1.10), Printer0  
  - **HR Dept (VLAN 20):** PC1 (192.168.2.10), Printer1  
  - **Finance Dept (VLAN 30):** PC2 (192.168.3.10), Printer2  
  - **Business Dept (VLAN 40):** PC3 (192.168.4.10), Printer3  

### Building B (192.168.5.0/24 – 192.168.6.0/24)
- **Switch-19 (2960-24TT)** uplinks to CoreSW  
  - **E&C Dept (VLAN 50):** PC4 (192.168.5.10), Printer4  
  - **Art & Design (VLAN 60):** PC5 (192.168.6.10), Printer5  

### Building C (192.168.7.0/24 – 192.168.9.0/24)
- **Switch-20 (2960-24TT)** for Student Lab  
  - Lab PCs (VLAN 70): 192.168.7.0/24, Printer6  
- **Switch-21 (2960-24TT)** for IT Room  
  - Web Server (VLAN 80): 192.168.8.10  
  - FTP Server (VLAN 80): 192.168.8.11  

### Smaller Campus (192.168.9.0/24 – 192.168.10.0/24)
- **3650-24PS (L3):** uplink to Core  
  - Staff LAN (VLAN 90): PC8 (192.168.9.10), Printer8  
  - Student LAN (VLAN 100): PC9 (192.168.10.10), Printer9  

### Small Building (192.168.11.0/24)
- **2960 (Access Switch):** PC10 (192.168.11.10), Printer10 (VLAN 110)

---

## 🎯 IP Addressing & VLAN Design

| Location           | Subnet             | VLAN ID | Devices                    |
| ------------------ | ------------------ | ------- | -------------------------- |
| Bldg A Mgmt        | 192.168.1.0 /24    | 10      | PC0, Printer0              |
| Bldg A HR          | 192.168.2.0 /24    | 20      | PC1, Printer1              |
| Bldg A Finance     | 192.168.3.0 /24    | 30      | PC2, Printer2              |
| Bldg A Business    | 192.168.4.0 /24    | 40      | PC3, Printer3              |
| Bldg B E&C         | 192.168.5.0 /24    | 50      | PC4, Printer4              |
| Bldg B Art & Des.  | 192.168.6.0 /24    | 60      | PC5, Printer5              |
| Bldg C Lab         | 192.168.7.0 /24    | 70      | PC6, Printer6              |
| Bldg C IT/Web      | 192.168.8.0 /24    | 80      | Web & FTP Servers          |
| Smaller Campus Stf | 192.168.9.0 /24    | 90      | PC8, Printer8              |
| Smaller Campus Std | 192.168.10.0 /24   | 100     | PC9, Printer9              |
| Small Building     | 192.168.11.0 /24   | 110     | PC10, Printer10            |

- **Trunks** carry VLANs 10–110 with 802.1Q tagging.  
- **Core Router** subinterfaces for each VLAN (inter-VLAN routing & Internet gateway).

---

## 🔧 Key Hardware Components

| Component                         | Role                                          |
| --------------------------------- | --------------------------------------------- |
| **Cisco 2911 Routers**            | Inter-building routing, static & dynamic RPs  |
| **Cisco 3850-24PS Core Switch**   | Multilayer switching, ACLs, QoS, VLANs        |
| **Cisco 3650-24PS (Smaller campus)** | L3 distribution for small campus            |
| **Cisco 2960-24TT Switches**      | Access switches for departments & labs        |
| **Servers:** Email, Web, FTP      | Centralized services on dedicated VLANs       |
| **Fiber/Copper Trunks**           | 10 Gbps links between Core & distribution     |
| **Cisco Packet Tracer**           | Simulation & testing                          |

---

## 🔄 Data Flow and Routing

1. **Inter-VLAN Access** (Finance → Web Server)  
   PC2 → Dept Switch → CoreSW → IT Switch → Web Server  

2. **Inter-Building Comm** (Mgmt → Art & Design)  
   PC0 → Switch-18 → Router0 → Switch-19 → PC5  

3. **Email Delivery**  
   Any PC → CoreSW → Router2 → Email Server  

4. **Internet Browsing**  
   All VLANs → CoreSW → Router0/1 → Campus Backbone → ISP  

---

## 🖼️ Images

**Figure 1: Campus Overall Topology**  
![Campus Overall Topology](/main.png)

**Figure 2: Building A Network Layout**  
![Building A Network Layout](/mainn.png)

**Figure 3: Small Building Network Layout**  
![Small Building Network Layout](/small.png)

**Figure 4: Router Configuration Overview**  
![Router Configuration Overview](/rout.png)

---

## 🔒 Security & Management

- **VLAN Segmentation:** Isolates departmental traffic  
- **ACLs on CoreSW:** Restrict inter-VLAN & server access  
- **Port Security:** Limits MACs per access port  
- **SNMP & NetFlow:** Central monitoring & analytics  
- **Redundancy:** Dual uplinks & STP root management  

---

## 🎯 Benefits & Scalability

- **Modular Expansion:** Add new buildings/VLANs with minimal design changes  
- **High Performance:** 10 Gbps trunks & L3 switching reduce latency  
- **Easy Troubleshooting:** Clear segmentation & monitoring  
- **Robust Security:** VLANs, ACLs, port security protect resources  

---

## 🛠️ Getting Started

1. **Clone the repository**  
   ```bash
   git clone https://github.com/Jhansi426/UNIVERSITY-NETWORK-USING-CISCO-PACKET-TRACER.git
   cd UNIVERSITY-NETWORK-USING-CISCO-PACKET-TRACER

2. **Open Packet Tracer file**

   * `university_network.pkt` in the root folder

3. **Review configs**

   * `/configs/routers/` for router CLI scripts
   * `/configs/switches/` for switch setups

4. **Simulate & Validate**

   * Verify VLAN tagging, inter-VLAN routing, server reachability

5. **Customize as needed**

   * Change VLAN IDs, subnets, add new services or buildings
   
