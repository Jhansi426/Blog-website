---
title: "Network Topologies Simulation using Cisco Packet Tracer"
description: "Simulate classic network topologies like Bus, Ring, Star, Mesh, and Tree using Cisco Packet Tracer with assigned IP ranges."
pubDate: "Jun 13 2025"
heroImage: "/bus.png"
badge: "Network Topologies"
tags: ["networking", "packet-tracer", "topologies"]
---

# NETWORK-TOPOLOGIES-SIMULATION-USING-CISCO-PACKET-TRACER

## 📖 Table of Contents

1. [Project Overview](#project-overview)  
2. [IP Addressing Scheme](#ip-addressing-scheme)  
3. [Simulated Topologies](#simulated-topologies)  
   - [Bus Topology](#bus-topology)  
   - [Ring Topology](#ring-topology)  
   - [Star Topology (Switch)](#star-topology-switch)  
   - [Star Topology (Hub)](#star-topology-hub)  
   - [Mesh Topology](#mesh-topology)  
   - [Tree Topology](#tree-topology)  
4. [Simulation Tool & Resources](#simulation-tool--resources)  
5. [Conclusion](#conclusion)

---

## 🚀 Project Overview

This project demonstrates the creation and simulation of **five classic network topologies** using **Cisco Packet Tracer**. Each topology follows standard networking principles and is built with appropriate interconnections, using switches, hubs, and routers as required.


The IP range utilized throughout the simulations is:

```

220.35.0.1 – 220.35.255.255

```

Each topology was constructed with a focus on network design clarity, basic configuration, and operational connectivity.

---

## 🧮 IP Addressing Scheme

The IP addresses assigned begin from **220.35.0.1** and are distributed incrementally for each device in all topologies. Subnetting was not emphasized in this simulation-focused assignment but can be extended in future configurations.

---

## 🕸️ Simulated Topologies

### 🚌 Bus Topology

- All devices connected via a single communication line.
- Simple, linear layout using straight-through cables.
- **Pros:** Easy to implement for small networks.  
- **Cons:** Prone to collisions, no redundancy.

**Figure:**  
![Bus Topology](/bus.png)

---

### 🔄 Ring Topology

- Devices connected in a closed loop.
- Each device forwards data to the next node.
- **Pros:** Equal access, predictable performance.  
- **Cons:** Single break disables entire network.
![ring Topology - Switch](/ring1.png)

---

### 🌟 Star Topology (Switch)

- Devices connected to a central switch.
- High-speed transmission and easy device isolation.
- **Pros:** Scalable, easy fault detection.  
- **Cons:** Central device failure risks full outage.

**Figure:**  
![Star Topology - Switch](/star.png)

---

### 🌟 Star Topology (Hub)

- Central hub broadcasts data to all devices.
- No switching intelligence, more collisions.
- **Pros:** Cost-effective, simple layout.  
- **Cons:** Less efficient than switch-based networks.

**Figure:**  
![Star Topology - Hub](/hub.png)

---

### 🔷 Mesh Topology

- Every device connects to every other device.
- Offers full redundancy and high fault tolerance.
- **Pros:** Resilient, multiple paths.  
- **Cons:** Complex, costly cabling.

**Figure:**  
![Mesh Topology](/mesh.png)

---

### 🌲 Tree Topology

- Hybrid structure combining star and bus topologies.
- Hierarchical structure with layered connectivity.
- **Pros:** Scalable, manageable hierarchy.  
- **Cons:** Root or central failures can affect branches.

**Figure:**  
![Tree Topology](/trree.png)

---

## 🛠️ Simulation Tool & Resources

| Tool/Resource          | Usage                            |
|------------------------|----------------------------------|
| **Cisco Packet Tracer**| Primary network design tool      |
| `.pkt` Files           | Saved simulations per topology   |
| IP Range: 220.35.x.x   | Assigned uniformly across nodes  |
| Devices Used           | PCs, Switches, Hubs, Routers     |

---

## ✅ Conclusion

This assignment reinforced key networking concepts by allowing hands-on simulation of core topologies in **Cisco Packet Tracer**. Each topology serves a distinct use-case in network design, and understanding their structure, benefits, and limitations is critical for real-world applications.

---
