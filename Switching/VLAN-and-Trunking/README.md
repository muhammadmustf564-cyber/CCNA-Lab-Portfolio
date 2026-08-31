# VLAN and Trunking — Cisco Packet Tracer

> **A practical switching lab demonstrating VLAN segmentation, trunking, and inter-switch connectivity using Cisco Packet Tracer.**

---

## 🔹 Lab Overview

This lab demonstrates how **VLANs segment a switched network into separate logical networks** and how **trunking enables multiple VLANs to travel between switches**.

The network contains **two switches, three VLANs, and twelve PCs**. The same VLANs are configured on both switches, allowing devices in the same VLAN to communicate across the trunk link while maintaining isolation from other VLANs.

---

## 🖧 Network Design

```text
                 ┌─────────────────┐
                 │    TRUNK LINK   │
                 │   VLAN 10,20,30 │
                 └────────┬────────┘
                          │
            ┌─────────────┴─────────────┐
            │                           │
       ┌────▼─────┐                ┌────▼─────┐
       │ Switch 1 │                │ Switch 2 │
       └────┬─────┘                └────┬─────┘
            │                           │
      ┌─────┼─────┐               ┌─────┼─────┐
      │     │     │               │     │     │
    VLAN 10 VLAN20 VLAN30        VLAN10 VLAN20 VLAN30
      │     │     │               │     │     │
     2 PCs  2 PCs  2 PCs          2 PCs  2 PCs  2 PCs
```

### VLAN Addressing

|  VLAN  |      Network      | Devices |
| :----: | :---------------: | :-----: |
| **10** | `192.168.10.0/24` |  4 PCs  |
| **20** | `192.168.20.0/24` |  4 PCs  |
| **30** | `192.168.30.0/24` |  4 PCs  |

Each VLAN has **two PCs on each switch**.

---

## ⚙️ What Was Configured

### 1. VLAN Segmentation

Three VLANs were created on both switches:

```text
VLAN 10
VLAN 20
VLAN 30
```

Access ports were assigned to the appropriate VLAN based on the connected PCs.

### 2. Switch-to-Switch Trunk

The connection between the two switches was configured as a **trunk port**.

The trunk carries traffic for:

```text
VLAN 10
VLAN 20
VLAN 30
```

This allows the same VLAN to span both switches.

---

## 🔎 Verification

### VLAN Verification

```bash
show vlan brief
```

Used to confirm VLAN creation and access-port assignments on both switches.

### Trunk Verification

```bash
show interfaces trunk
```

Used to confirm that the inter-switch connection is operating as a trunk and carrying the required VLANs.

---

## 🧪 Connectivity Tests

### ✅ Same VLAN — Successful

A **VLAN 20 PC** was used to ping another **VLAN 20 PC** located on the other switch.

**Result:** `SUCCESS`

This confirms that VLAN 20 traffic is successfully crossing the trunk link.

### ❌ Different VLAN — Blocked

A **VLAN 20 PC** was then used to ping a **VLAN 30 PC**.

**Result:** `FAILED`

This is expected because VLAN 20 and VLAN 30 are separate broadcast domains.

> **Inter-VLAN communication requires a Layer 3 device such as a router or Layer 3 switch.**

---

## 📸 Lab Evidence

| Screenshot                   | Verification                                 |
| :--------------------------- | :------------------------------------------- |
| `01-Topology.png`            | Complete network topology                    |
| `02-VLAN-Configuration.png`  | VLAN configuration on both switches          |
| `03-Trunk-Configuration.png` | Trunk configuration and verification         |
| `04-Ping-Verification.png`   | Same-VLAN success + different-VLAN isolation |

---

## 🧠 Key Takeaways

* VLANs provide **logical network segmentation**.
* Access ports belong to a specific VLAN.
* Trunk ports can carry **multiple VLANs** between switches.
* The same VLAN can communicate across multiple switches through a trunk.
* Different VLANs are isolated by default.
* **Inter-VLAN routing** is required for communication between different VLANs.

---

## 🛠️ Tools & Technologies

**Cisco Packet Tracer** · **Cisco IOS CLI** · **VLANs** · **802.1Q Trunking** · **Switching**

## 📁 Lab Files
```text
VLAN-and-Trunking/
│
├── screenshots/
│   ├── 01-Topology.png
│   ├── 02-VLAN-Configuration.png
│   ├── 03-Trunk-Configuration.png
│   └── 04-Ping-Verification.png
│
├── README.md
└── VLAN-and-Trunking.pkt
```


### Status

**Completed ✓ | Configured ✓ | Tested ✓ | Verified ✓**

