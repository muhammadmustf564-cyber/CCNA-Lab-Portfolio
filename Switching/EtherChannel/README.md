```markdown
# 🔗 EtherChannel Lab

> **CCNA Switching Lab | Cisco Packet Tracer**

## 📌 Overview

This lab demonstrates the configuration, verification, and failover testing of **EtherChannel** between Cisco switches.

EtherChannel combines multiple physical links into **one logical Port-Channel**, providing **redundancy, improved bandwidth utilization, and simplified network management**.

---

## 🎯 Objectives

- Configure VLANs on Cisco switches
- Configure EtherChannel between switches
- Configure EtherChannel as a trunk
- Verify EtherChannel formation
- Test VLAN connectivity
- Perform EtherChannel failover testing
- Verify network behavior after a member-link failure

---

## 🗺️ VLAN & IP Network Plan

| VLAN | IP Network |
|------|------------|
| VLAN 10 | `192.168.10.0/24` |
| VLAN 20 | `192.168.20.0/24` |
| VLAN 30 | `192.168.30.0/24` |

---

## 🔗 EtherChannel Concept

Multiple physical links were bundled together into a single logical interface:

    Physical Links
         │
         ├── Link 1
         ├── Link 2
         ├── Link 3
         └── Link 4
              │
              ▼
       ┌──────────────┐
       │ Port-Channel │
       └──────────────┘
              │
              ▼
        Logical Link

This allows the switches to treat multiple physical connections as **one logical link**.

---

## ⚙️ Configuration

### VLANs

The following VLANs were configured:

- **VLAN 10**
- **VLAN 20**
- **VLAN 30**

### EtherChannel

Multiple physical interfaces were bundled into a **Port-Channel**.

The Port-Channel was configured as a **trunk** so that multiple VLANs could traverse the EtherChannel.

---

## 🔍 Verification

### EtherChannel Status

    show etherchannel summary

This command was used to verify the Port-Channel and its member interfaces.

### Trunk Verification

    show interfaces trunk

This command was used to verify trunk operation and VLAN propagation.

---

## 🧪 Connectivity Testing

Connectivity was tested using ping from Switch 0.

### Test 1

    ping 192.168.30.2

✅ Successful

### Test 2

    ping 192.168.20.3

✅ Successful

These tests confirmed connectivity across the configured network.

---

## 🔥 EtherChannel Failover Test

To test redundancy, one member link was intentionally shut down.

    interface fa0/1
    shutdown

The EtherChannel status was then checked:

    show etherchannel summary

The remaining member links continued to provide connectivity.

### Result

**One physical link failed → EtherChannel remained operational through the remaining links.** ✅

---

## 🧠 Key Concepts Learned

- **EtherChannel** combines multiple physical links into one logical link.
- **Port-Channel** represents the logical EtherChannel interface.
- EtherChannel can provide **redundancy** when multiple physical links are available.
- A trunk EtherChannel can carry traffic from **multiple VLANs**.
- `show etherchannel summary` is used to verify EtherChannel status.
- A single member-link failure does not necessarily bring down the entire EtherChannel.

---

## 📸 Lab Evidence

| # | Evidence |
|---|----------|
| 01 | EtherChannel Topology |
| 02 | EtherChannel Summary |
| 03 | Trunk Verification |
| 04 | Successful Ping Tests |
| 05 | EtherChannel Failover Test |

---

## 📁 Project Files

    EtherChannel/
    ├── EtherChannel_Lab.pkt
    ├── 01_EtherChannel_Topology.png
    ├── 02_SW1_EtherChannel_Summary.png
    ├── 03_SW0_Trunk_Verification.png
    ├── 04_SW0_Ping_Test.png
    ├── 05_SW2_EtherChannel_Failover.png
    └── README.md

---

## 🛠️ Tools Used

- **Cisco Packet Tracer**
- **Cisco IOS CLI**

---

## 🚀 Skills Practiced

`VLANs` · `EtherChannel` · `Port-Channel` · `Trunking` · `Redundancy` · `Failover` · `Network Verification` · `Cisco IOS`

---

### 📚 CCNA Lab Portfolio

Part of my **CCNA Networking Lab Portfolio**, focused on building practical networking skills through Cisco Packet Tracer labs.
```
