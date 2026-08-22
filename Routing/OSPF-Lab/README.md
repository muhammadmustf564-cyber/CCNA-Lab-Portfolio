# OSPF Multi-Area Routing Lab

## 📌 Overview

This lab demonstrates **Open Shortest Path First (OSPF) multi-area dynamic routing** using Cisco Packet Tracer.

The topology consists of multiple routers divided into **OSPF Area 0 (Backbone Area)** and **Area 1**. Router4 operates as the **Area Border Router (ABR)**, connecting Area 0 with Area 1.

The lab focuses on OSPF neighbor formation, interface verification, route learning, and multi-area OSPF design.

---

## 🎯 Objectives

* Configure OSPF dynamic routing
* Understand OSPF Area 0 and Area 1
* Configure and verify an Area Border Router (ABR)
* Establish OSPF neighbor relationships
* Verify OSPF-learned routes
* Verify router interface status
* Understand communication between multiple OSPF areas

---

## 🛠️ Tools & Technologies

* **Cisco Packet Tracer**
* **Cisco IOS**
* **OSPF**
* **IPv4**
* **Serial Interfaces**
* **Dynamic Routing**

---

## 🌐 Network Topology

The topology contains six routers divided into two OSPF areas.

![OSPF Network Topology](Screenshots/OSPF-Topology.png)

---

## 🔷 OSPF Area Design

### Area 0 — Backbone Area

The following routers are configured in **OSPF Area 0**:

* Router0
* Router1
* Router2
* Router3

Area 0 serves as the **OSPF backbone area**.

### Area 1

The following router is configured in **OSPF Area 1**:

* Router5

### Area Border Router — Router4

**Router4 acts as the Area Border Router (ABR).**

Router4 connects **Area 0 and Area 1**, allowing OSPF routing information to be exchanged between the two areas.

### Area Summary

| OSPF Area       | Routers                            | Role                     |
| --------------- | ---------------------------------- | ------------------------ |
| Area 0          | Router0, Router1, Router2, Router3 | Backbone routers         |
| Area 1          | Router5                            | Area 1 router            |
| Area 0 + Area 1 | Router4                            | Area Border Router (ABR) |

---

## 🔍 OSPF Verification

The following Cisco IOS commands were used to verify the OSPF implementation.

### Interface Verification

```bash
show ip interface brief
```

Used to verify interface status and IP addressing.

### OSPF Neighbor Verification

```bash
show ip ospf neighbor
```

Used to verify OSPF neighbor relationships and confirm that routers have established OSPF adjacencies.

### OSPF Route Verification

```bash
show ip route ospf
```

Used to identify routes learned dynamically through OSPF.

### OSPF Configuration Verification

```bash
show running-config | section router ospf
```

Used to verify the OSPF routing process and area configuration.

---

## 📸 Verification Screenshots

### Router1 — OSPF Verification

![Router1 OSPF Verification](Screenshots/Router1-OSPF-Verification.png)

### Router2 — OSPF Verification

![Router2 OSPF Verification](Screenshots/Router2-OSPF-Verification.png)

### Router4 — OSPF ABR Verification

![Router4 OSPF Verification](Screenshots/Router4-OSPF-Verification.png)

---

## 🧠 Key Concepts Demonstrated

### OSPF Neighbor Formation

OSPF routers establish neighbor relationships to exchange routing information and maintain the OSPF topology.

### OSPF Area 0

Area 0 is the **backbone area** of the OSPF topology. Other OSPF areas communicate through the backbone.

### Area Border Router (ABR)

Router4 connects **Area 0 and Area 1** and therefore operates as an **ABR**.

### Dynamic Route Learning

OSPF dynamically learns remote networks and installs the best available routes into the routing table.

---

## ✅ Verification Checklist

* [x] OSPF configured on routers
* [x] Area 0 configured as the backbone area
* [x] Area 1 configured
* [x] Router4 configured as the ABR
* [x] OSPF neighbor relationships verified
* [x] OSPF routes verified
* [x] Router interfaces verified
* [x] Topology documented

---

## 📚 Learning Outcome

This lab provided hands-on experience with **multi-area OSPF**, including OSPF neighbor formation, dynamic route learning, backbone and non-backbone areas, and the role of an **Area Border Router (ABR)**.

It also strengthened practical Cisco IOS troubleshooting and verification skills using OSPF show commands.

---

## 🧪 Lab Status

**Status:** Completed ✅

**Platform:** Cisco Packet Tracer

**Routing Protocol:** OSPF

**OSPF Areas:** Area 0 & Area 1

**ABR:** Router4

**Addressing:** IPv4

**Lab Type:** Multi-Area Dynamic Routing

