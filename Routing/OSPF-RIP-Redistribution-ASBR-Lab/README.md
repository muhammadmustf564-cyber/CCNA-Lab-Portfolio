### OSPF ↔ RIP Redistribution Using ASBR
## 📌 Lab Overview

This lab demonstrates route redistribution between OSPF and RIP using an ASBR (Autonomous System Boundary Router).

The network is divided into two routing domains:

OSPF Area 0 — OSPF routers
RIP Network — RIP routers
R0 acts as the ASBR between both routing protocols.
🎯 Objectives
Configure OSPF Area 0.
Configure RIP.
Configure R0 as an ASBR.
Redistribute RIP routes into OSPF.
Redistribute OSPF routes into RIP.
Verify routing tables and OSPF neighbors.
Test end-to-end connectivity between both routing domains.
🌐 Network Design
              OSPF Area 0
                   
R6 ───── R2 ───── R1 ───── R0
                           │
                         ASBR
                           │
                           │
                      RIP Network
                           │
                         R3 ───── R4
⚙️ Redistribution Configuration
OSPF → RIP

R0 redistributes OSPF routes into RIP:

router rip
 redistribute ospf 1 metric 2
RIP → OSPF

R0 redistributes RIP routes into OSPF:

router ospf 1
 redistribute rip subnets
🔍 Verification

The following commands were used to verify the configuration:

show ip route
show ip ospf neighbor
show ip protocols
show running-config | section router ospf
show running-config | section router rip
🧪 Connectivity Testing
RIP-side Network
ping 30.0.0.1

✅ Successful connectivity from the OSPF side to the RIP network.

OSPF-side Network
ping 1.1.1.1

✅ Successful connectivity from the RIP side to the OSPF network.

📸 Lab Evidence
01-Topology.png — Network topology
02-Show-IP-Route.png — Routing table verification
03-OSPF-RIP-Running-Config.png — OSPF and RIP redistribution configuration
04-OSPF-Neighbors.png — OSPF neighbor verification
05-Show-IP-Protocols.png — Routing protocol verification
06-Ping-RIP-30.0.0.1.png — Connectivity to RIP network
07-Ping-OSPF-1.1.1.1.png — Connectivity to OSPF network
🛠️ Tools
Cisco Packet Tracer
Cisco IOS CLI
📚 Key Concepts Learned
OSPF Area 0
RIP
ASBR
Route Redistribution
OSPF Neighbor Adjacency
Routing Table Verification
End-to-End Connectivity Testing
