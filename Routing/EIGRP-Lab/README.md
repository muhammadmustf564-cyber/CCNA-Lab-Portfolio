# EIGRP Routing Lab

## 📌 Overview

This lab demonstrates the configuration and verification of **Enhanced Interior Gateway Routing Protocol (EIGRP)** in a multi-router network using Cisco Packet Tracer.

The lab focuses on configuring EIGRP, establishing neighbor relationships, learning routes dynamically, and verifying network connectivity.

## 🎯 Objectives

• Configure EIGRP on multiple routers
• Establish EIGRP neighbor relationships
• Advertise networks using EIGRP
• Verify EIGRP-learned routes
• Examine the EIGRP topology table
• Verify interface bandwidth and delay
• Test end-to-end connectivity


## 🛠️ Tools Used

- Cisco Packet Tracer
- Cisco IOS CLI

## ⚙️ EIGRP Configuration

EIGRP was configured on the routers using the following commands:

```bash
router eigrp <AS-number>
network <network-address>

🔍 Verification Commands

The following commands were used to verify the configuration and operation of EIGRP:

- show ip interface brief
- show running-config | section router eigrp
- show ip eigrp neighbors
- show ip route
- show ip eigrp topology
- show interfaces s0/1/0
- ping 192.168.1.3

✅ Verification

The lab was verified by:

- Checking interface status
- Confirming EIGRP configuration
- Verifying EIGRP neighbor relationships
- Checking dynamically learned routes
- Examining the EIGRP topology table
- Checking interface bandwidth and delay values
- Testing connectivity between networks

🏁 Result

EIGRP was successfully configured and verified across the multi-router topology. EIGRP neighbor relationships were established, routes were dynamically learned, and end-to-end connectivity was successfully verified using ICMP ping.



