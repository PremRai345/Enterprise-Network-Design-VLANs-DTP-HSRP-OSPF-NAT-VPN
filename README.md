# Enterprise-Network-Design-VLANs-DTP-HSRP-OSPF-NAT-VPN
Enterprise multi-site network design using Cisco Packet Tracer featuring VLANs, DTP, HSRP, OSPF, NAT, VPN
# Enterprise Multi-Site Network Design (Cisco Packet Tracer)

## 📌 Overview
This project demonstrates the design and implementation of a real-world enterprise network topology using Cisco Packet Tracer.  
The network simulates a Head Office (HQ) and a Branch Office connected securely over a public ISP using a GRE tunnel VPN.

The lab focuses on core enterprise networking concepts such as VLAN segmentation, high availability, dynamic routing, NAT, and site-to-site connectivity.

---

## 🏗️ Network Architecture
- Multi-tier campus network (Access, Distribution, Core)
- Separate HQ and Branch Office networks
- Public ISP for internet simulation
- Site-to-site GRE VPN over public internet

---

## 🧩 Technologies & Features Implemented

### LAN & Switching
- VLANs: 10 (HR), 20 (Marketing), 30 (IT)
- Inter-VLAN routing using multilayer switches (SVIs)
- 802.1Q trunking between access and distribution switches

### High Availability
- HSRP for default gateway redundancy
- Active/Standby multilayer switch configuration
- Priority and preemption configuration

### Routing
- OSPF for dynamic routing between distribution, core, and edge devices
- Passive interfaces configured where appropriate
- Default route redistribution into OSPF

### WAN & Internet Access
- NAT (PAT) configured on edge routers
- Internal users and servers can access the internet
- Public IP addressing simulated via ISP router

### VPN Connectivity
- GRE tunnel configured between HQ and Branch edge routers
- Tunnel IP network: 172.16.1.0/30
- OSPF enabled over GRE tunnel for private network reachability

### Services & Testing
- HTTP, FTP, and TFTP servers at Branch Office
- End-to-end connectivity testing using ICMP
- Validation of failover, routing, and VPN functionality

---

## 🖥️ IP Addressing Summary

| Network | Purpose |
|-------|--------|
| 192.168.10.0/24 | HR VLAN |
| 192.168.20.0/24 | Marketing VLAN |
| 192.168.30.0/24 | IT VLAN |
| 10.1.1.0/24 | Branch Office LAN |
| 172.16.1.0/30 | GRE Tunnel |
| 100.1.1.0/30 | HQ ↔ ISP |
| 101.1.1.0/30 | Branch ↔ ISP |

---

## 📂 Files Included
- `enterprise_network.pkt` – Cisco Packet Tracer lab file
- `enterprise_network_topology.png` – Network topology diagram
- `configs/` – Device configuration files (CLI)
- `notes/` – Design explanations and observations

---

## 🧠 Key Learning Outcomes
- Enterprise VLAN and redundancy design
- HSRP behavior and failover concepts
- Dynamic routing with OSPF
- NAT inside/outside translation
- Site-to-site GRE VPN configuration
- Real-world troubleshooting and validation

---

## 🚀 Future Improvements
- Add ACLs for inter-VLAN security
- Implement IPsec over GRE
- Add monitoring (SNMP, Syslog)
- Convert lab to GNS3 / EVE-NG

---

