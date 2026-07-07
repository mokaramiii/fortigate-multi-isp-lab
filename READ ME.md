# FortiGate Static Routing & Policy Routing Lab

## Overview

This lab demonstrates how to configure Static Routing, Administrative Distance, Policy-Based Routing (PBR), NAT, and ISP Failover using FortiGate.

The topology consists of multiple VLANs, Layer 3 switches, three ISP routers, one TCI ISP, and a FortiGate firewall acting as the edge device.

---

## Lab Topology

> Add the topology image here.

![Topology](images/topology.png)

---

## Objectives

This lab was designed around four simple tasks.

### Task 1
Provide Internet access for all users through **ISP1**.

---

### Task 2
Configure ISP Failover using Static Routes.

- ISP1 → Distance 10
- ISP2 → Distance 20
- ISP3 → Distance 30

If ISP1 becomes unavailable, traffic automatically switches to ISP2, and then to ISP3.

---

### Task 3
Implement Policy-Based Routing (PBR).

- User networks use different ISPs.
- Infrastructure networks use the TCI provider.

---

### Task 4
Configure source-based Internet access.

| Network | Outgoing ISP |
|----------|--------------|
| VLAN10 | ISP1 |
| VLAN20 | ISP1 |
| VLAN30 | ISP2 |
| VLAN40 | ISP3 |
| INFRA | TCI (Primary: Port7 / Backup: Port8) |

---

## Technologies Used

- FortiGate Firewall
- Static Routing
- Administrative Distance
- Policy-Based Routing (PBR)
- Firewall Policies
- NAT (IP Pool)
- ISP Failover
- Traffic Logs
- Debug Flow
- Troubleshooting

---

## Verification

The following tests were performed successfully:

- Internet access from all VLANs
- Static Route Failover
- Policy-Based Routing
- NAT verification
- TCI Primary/Backup routing
- Routing table verification
- Traffic log verification
- Debug Flow analysis

---

## Troubleshooting

During the lab, the following issues were identified and resolved:

- Implicit Deny
- Missing Firewall Policies
- Incorrect Source Address Objects
- Reverse Path Check
- Policy Route matching
- Static Route priority
- NAT verification

---

## Author

**Mohammad Karami**

This lab was created for learning and practicing FortiGate routing concepts in a multi-ISP environment.