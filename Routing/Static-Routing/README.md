# Static Routing Lab

## 📌 Overview

This lab demonstrates the configuration of static routing using Cisco Packet Tracer. Multiple routers were configured with static routes to enable communication between different networks.

Connectivity was verified using ping and traceroute to confirm successful end-to-end communication.

## 🎯 Objectives

- Configure IP addresses on routers and end devices
- Configure static routes on multiple routers
- Verify static routes using `show ip route`
- Test connectivity between different networks using `ping`
- Verify the packet path using `tracert`

## 🛠️ Tools Used

- Cisco Packet Tracer
- Routers
- PCs
- Laptop

## ⚙️ Configuration

Static routes were configured on the routers using the following command:

```bash
ip route <destination-network> <subnet-mask> <next-hop-ip>

The routing tables were verified using:

show ip route

Static routes are identified by the letter S in the routing table.

## 🧪 Verification 

Connectivity was tested using ping, and the packet path was verified using tracert.

Ping Tests
PC1 → PC2
PC1 → PC4
Traceroute Test
PC1 → Laptop (10.0.0.4)

The tests confirmed successful communication between different networks and verified the path taken by packets through the routers.

## **📸 Screenshots**
1. Network Topology

2. Router 1 Routing Table

3. Router 2 Routing Table

4. Router 3 Routing Table

5. Router 4 Routing Table

6. PC1 to PC2 Ping

7. PC1 to PC4 Ping

8. PC1 to Laptop Tracert

✅ Result

Static routing was successfully configured and verified. Communication between different networks was successfully established.

The routing tables, ping tests, and traceroute results confirmed that packets could successfully travel between the configured networks.

📚 Key Learning
• Static Routing
• Routing Tables
• Next-Hop Routing
• Network Connectivity
• Ping Testing
• Traceroute
• Basic Network Troubleshooting
