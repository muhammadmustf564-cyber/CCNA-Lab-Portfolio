# RIP (Routing Information Protocol) Lab

## 📌 Overview

This lab demonstrates the configuration of **RIP (Routing Information Protocol)** in a multi-router network using Cisco Packet Tracer.

## 🎯 Objectives

* Configure RIP on multiple routers
* Advertise directly connected networks
* Verify RIP configuration and dynamically learned routes
* Test connectivity between remote networks

## 🛠️ Tools Used

* Cisco Packet Tracer
* Cisco Routers

## ⚙️ Configuration

RIP was configured on all routers using their directly connected networks.

```bash
router rip
network <network-address>
```

## 🔍 Verification

RIP configuration was verified using:

```bash
show running-config | section router rip
```

The routing table was checked using:

```bash
show ip route
```

Connectivity between remote networks was verified using:

```bash
ping <destination-ip>
```

## 📸 Screenshots

### Network Topology

![RIP Topology](Routing/RIP/2-RIP-Topology.png)

### RIP Configuration

![RIP Configuration](RIP-Configuration.png)

### Routing Table

![RIP Routing Table](RIP-Routing-Table.png)

### Successful Ping

![Successful Ping](RIP-Successful-Ping.png)

## ✅ Result

RIP successfully exchanged routing information between the routers, and connectivity to remote networks was verified successfully.

