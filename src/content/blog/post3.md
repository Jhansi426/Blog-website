---
title: "Three Network Topologies Simulation using Cisco Packet Tracer"
description: "Simulate Tree, Star, and Ring topologies as separate LANs interconnected via a single router using Cisco Packet Tracer."
pubDate: "Jun 14 2025"
heroImage: "/over.png"
badge: "Router-Based Topologies"
tags: ["packet-tracer","networking", "topologies", "router"]
---

# INTERCONNECTING-LAN-TOPOLOGIES-VIA-ROUTER

## 📖 Table of Contents

1. [Project Overview](#project-overview)  
2. [IP Addressing Scheme](#ip-addressing-scheme)  
3. [Topology Setup & Configuration](#topology-setup--configuration)  
   - [Star Topology](#star-topology)  
   - [Ring Topology](#ring-topology)  
   - [Tree Topology](#tree-topology)  
4. [Router Configuration](#router-configuration)  
5. [Ping Test & Results](#ping-test--results)  
6. [Conclusion](#conclusion)

---

## 🚀 Project Overview

This assignment focuses on simulating **three LAN networks**—each with a unique topology (Star, Ring, Tree)—and interconnecting them using a **single router** in **Cisco Packet Tracer**. It highlights practical aspects of topology setup, IP addressing, and inter-network communication using router configuration.

---

## 🧮 IP Addressing Scheme

| Topology | Color Code | IP Range                | Devices |
|----------|------------|--------------------------|---------|
| Star     | Blue       | 220.35.0.1 – 220.35.0.4   | 4       |
| Ring     | Yellow     | 220.35.1.1 – 220.35.1.4   | 4       |
| Tree     | Orange     | 220.35.2.1 – 220.35.2.6   | 6       |

Each subnet was independently assigned and routed through the central router to maintain segmented but connected networks.

---

## 🕸️ Topology Setup & Configuration

### 🌟 Star Topology

- 4 PCs connected to a central switch.
- Subnet: 220.35.0.x
- Blue-filled nodes in the simulation.

### 🔄 Ring Topology

- 4 PCs connected in a circular fashion using switches or point-to-point links.
- Subnet: 220.35.1.x
- Yellow-filled nodes.

### 🌲 Tree Topology

- 6 PCs connected hierarchically, mimicking organizational layers.
- Subnet: 220.35.2.x
- Orange-filled nodes.

---

## 🔌 Router Configuration

Each LAN was connected to a separate interface on a central router, and proper IP addresses were assigned.

- Router Interface 0 ➝ Star Network  
- Router Interface 1 ➝ Ring Network  
- Router Interface 2 ➝ Tree Network  

Static routing or interface-based routing was used to allow communication between subnets.
**Figure:**  
![Star Topology - Switch](/1.png)
**Figure:**  
![Ring Topology - Switch](/2.png)
**Figure:**  
![Tree Topology - Switch](/3.png)


---

## 🧪 Ping Test & Results

To validate connectivity, ping tests were conducted between nodes of different LANs:

- ✅ From **Star to Ring:** `220.35.0.1 ➝ 220.35.1.1`
**Figure:**
![Star to Ring - Switch](/4.png)  
- ✅ From **Ring to Tree:** `220.35.1.1 ➝ 220.35.2.1`  
**Figure:**  
![Ring Topology - Switch](/5.png)
- ⚠️ From **Tree to Star:** `221.35.2.1 ➝ 221.35.0.1` 
**Figure:**  
![Tree Topology - Switch](/6.png)
---

## ✅ Conclusion

This simulation project successfully demonstrates:

- ✔ The setup of multiple distinct LAN topologies in one simulation.  
- ✔ Use of IP subnetting for LAN separation.  
- ✔ Router configuration to facilitate inter-LAN communication.  
- ⚠ Highlighted the importance of correct IP planning to avoid mismatches.  

---

> 📘 **Learning Outcome:** Students gained practical understanding of router-based LAN interconnection, topology implementation, and addressing strategy in Cisco Packet Tracer.

