# 🔀 Inter-VLAN Routing Lab

> A Cisco Packet Tracer lab demonstrating communication between multiple VLANs and different IP subnets using **Router-on-a-Stick Inter-VLAN Routing**.

---

## 📌 Project Overview

In this lab, I configured **Inter-VLAN Routing** to allow devices in different VLANs and different IP subnets to communicate through a router.

The topology contains:

- 🖥️ Multiple PCs
- 🔀 Two Cisco switches
- 🌐 One router
- 🏷️ VLAN 10, VLAN 20, and VLAN 30
- 🔗 Trunk links between switches and the router
- 📡 Router sub-interfaces for Inter-VLAN Routing

---

## 🎯 Objectives

- Create and configure multiple VLANs
- Assign switch ports to the correct VLANs
- Configure trunk links
- Configure router sub-interfaces
- Assign different IP subnets to each side of the topology
- Configure default gateways
- Enable communication between different VLANs
- Verify connectivity using `ping`

---

## 🗺️ Network Topology

    PC  ─── Switch 0 ─── Router ─── Switch 1 ─── PC
           VLAN 10/20/30          VLAN 10/20/30
                    │                 │
                  Trunk             Trunk

---

## 🏷️ VLAN & IP Addressing

### 🔹 Left Side — Switch 0

| VLAN | Network | Default Gateway |
|------|---------|-----------------|
| VLAN 10 | `10.0.1.0/24` | `10.0.1.1` |
| VLAN 20 | `10.0.2.0/24` | `10.0.2.1` |
| VLAN 30 | `10.0.3.0/24` | `10.0.3.1` |

### 🔹 Right Side — Switch 1

| VLAN | Network | Default Gateway |
|------|---------|-----------------|
| VLAN 10 | `10.0.4.0/24` | `10.0.4.1` |
| VLAN 20 | `10.0.5.0/24` | `10.0.5.1` |
| VLAN 30 | `10.0.6.0/24` | `10.0.6.1` |

> **Note:** The VLAN IDs are the same on both switches, but the IP subnets are different. This allows the router to route between the different networks.

---

## 🌐 Router Sub-Interfaces

### 🔹 Left Side — `Fa0/0`

| Sub-Interface | VLAN | IP Address |
|---------------|------|------------|
| `Fa0/0.1` | VLAN 10 | `10.0.1.1/24` |
| `Fa0/0.2` | VLAN 20 | `10.0.2.1/24` |
| `Fa0/0.3` | VLAN 30 | `10.0.3.1/24` |

### 🔹 Right Side — `Fa0/1`

| Sub-Interface | VLAN | IP Address |
|---------------|------|------------|
| `Fa0/1.1` | VLAN 10 | `10.0.4.1/24` |
| `Fa0/1.2` | VLAN 20 | `10.0.5.1/24` |
| `Fa0/1.3` | VLAN 30 | `10.0.6.1/24` |

---

## ⚙️ Key Configuration

### Router Sub-Interfaces

The router uses sub-interfaces to provide Layer 3 gateways for the VLANs.

Example configuration:

    interface fa0/0.1
     encapsulation dot1Q 10
     ip address 10.0.1.1 255.255.255.0

    interface fa0/0.2
     encapsulation dot1Q 20
     ip address 10.0.2.1 255.255.255.0

    interface fa0/0.3
     encapsulation dot1Q 30
     ip address 10.0.3.1 255.255.255.0

The same concept is applied to the `Fa0/1` sub-interfaces for the right-side networks.

---

## 🔗 Trunking

The switch-to-router connections carry multiple VLANs, so the links are configured as **trunk links**.

The trunk allows VLAN 10, VLAN 20, and VLAN 30 traffic to reach the appropriate router sub-interface.

---

## 🧪 Verification

The configuration was tested using ICMP `ping`.

### Test 1 — Left VLAN 10 → Right VLAN 30

    Source:       10.0.1.2
    Destination:  10.0.6.2
    Result:       Successful

### Test 2 — Left VLAN 10 → Left VLAN 30

    Source:       10.0.1.2
    Destination:  10.0.3.3
    Result:       Successful

These successful ping tests demonstrate that the router is forwarding traffic between different IP networks.

---

## 📸 Screenshots

| # | Screenshot | Description |
|---|------------|-------------|
| 01 | `01_Inter-VLAN-Routing-Topology.png` | Complete network topology |
| 02 | `02_Left-Switch-VLAN-Configuration.png` | VLAN configuration on left switch |
| 03 | `03_Right-Switch-VLAN-Configuration.png` | VLAN configuration on right switch |
| 04 | `04_Router-Subinterface-Configuration.png` | Router sub-interface configuration |
| 05 | `05_Router-Routing-Table.png` | Router routing table |
| 06 | `06_Inter-VLAN-Ping-Verification.png` | Successful connectivity tests |

---

## 📂 Project Files

    Inter-VLAN-Routing/
    │
    ├── Inter-VLAN-Routing-Lab.pkt
    │
    ├── 01_Inter-VLAN-Routing-Topology.png
    ├── 02_Left-Switch-VLAN-Configuration.png
    ├── 03_Right-Switch-VLAN-Configuration.png
    ├── 04_Router-Subinterface-Configuration.png
    ├── 05_Router-Routing-Table.png
    └── 06_Inter-VLAN-Ping-Verification.png

---

## 🧠 Key Takeaways

- **VLAN** → logically separates devices into different broadcast domains.
- **Trunk** → carries traffic for multiple VLANs over one link.
- **Sub-interface** → provides a Layer 3 gateway for a specific VLAN.
- **Default Gateway** → forwards traffic outside the local subnet.
- **Inter-VLAN Routing** → allows devices in different VLANs/subnets to communicate through a Layer 3 device.
- **Router-on-a-Stick** → uses multiple router sub-interfaces to route traffic between VLANs.

---

## 🛠️ Tools Used

- **Cisco Packet Tracer**
- Cisco Router
- Cisco Switches
- PCs
- VLANs
- 802.1Q Trunking
- Router-on-a-Stick

---

## ✅ Result

The Inter-VLAN Routing lab was successfully configured and tested.

Devices from different VLANs and different IP subnets were able to communicate successfully through the router.

---

### 📚 CCNA Lab Portfolio

**Topic:** Switching & Inter-VLAN Routing  
**Platform:** Cisco Packet Tracer  
**Status:** ✅ Completed