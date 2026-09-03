# 🔄 VTP (VLAN Trunking Protocol) Lab

> 🚀 A Cisco Packet Tracer lab demonstrating **VTP Server, Transparent, and Client modes** in a multi-switch network.

---

## 🌐 Network Overview

This lab demonstrates how **VLAN Trunking Protocol (VTP)** can be used to manage VLAN information across multiple switches.

The network consists of **four switches**, each configured with a specific VTP role:

```text
                    VTP DOMAIN
                        │
                        ▼
   ┌──────────┐    ┌──────────────┐    ┌─────────┐    ┌─────────┐
   │ Switch0  │────│   Switch1    │────│ Switch2│────│ Switch3│
   │  SERVER  │    │ TRANSPARENT  │    │ CLIENT │    │ CLIENT │
   └──────────┘    └──────────────┘    └─────────┘    └─────────┘
