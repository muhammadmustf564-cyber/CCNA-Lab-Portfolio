# Standard ACL Implementation and Traffic Filtering

## Project Overview
This project demonstrates the implementation of Standard Access Control Lists (ACLs) in Cisco Packet Tracer using three routers and six PCs. The purpose is to control network traffic by filtering packets based on source IP addresses.

## Network Topology
- 3 Routers
- 6 PCs (2 PCs connected to each router)
- Network 10
- Network 20
- Network 30

## Objectives
- Block all traffic originating from Network 10 and destined for Network 30.
- Block traffic from a specific host (20.0.0.1) in Network 20 to Network 10.
- Permit all other traffic.

## ACL Configurations

### 1. Blocking Network 10 from Network 30
**Configured on Router 3:**

```cisco
access-list 1 deny 10.0.0.0 0.255.255.255
access-list 1 permit any

interface f0/0
ip access-group 1 out
```

### 2. Blocking Specific Host 20.0.0.1 from Network 10
**Configured on Router 1:**

```cisco
access-list 1 deny 20.0.0.1 0.0.0.0
access-list 1 permit any

interface f0/0
ip access-group 1 out
```

## Testing and Verification
- Verified that traffic from Network 10 to Network 30 is blocked.
- Tested permitted traffic between other networks.
- Verified that Host 20.0.0.1 cannot send traffic into Network 10.
- Tested connectivity from other permitted hosts.

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI
- Standard Access Control Lists

## Project Files
- `Standard-ACL-Lab.pkt` – Complete Packet Tracer topology and configurations.
- `Screenshots/` – ACL configurations, interface placement, and connectivity tests.

## Key Learning Outcomes
- Understanding Standard ACLs.
- Configuring ACLs using wildcard masks.
- Applying ACLs to router interfaces.
- Understanding IN and OUT directions.
- Filtering traffic based on source IP addresses.
- Verifying network connectivity and access restrictions.

---

**Project Type:** Networking / CCNA Lab  
**Technology:** Cisco Packet Tracer