# enterprise-network-security-simulation

# Enterprise Network Design & Security Simulation

## Overview

This project simulates a real-world enterprise network using GNS3, Cisco networking devices, and a FortiGate Firewall.

The objective was to design a secure and scalable network infrastructure capable of supporting multiple departments while maintaining network segmentation, centralized IP address management, secure Internet access, and traffic control through firewall policies.

The network includes VLAN implementation, Inter-VLAN Routing, DHCP services, FortiGate security policies, and end-to-end connectivity verification.

---

## Network Topology

Internet connectivity is simulated through an ISP router (R1).

Traffic passes through a FortiGate Firewall before reaching the internal enterprise network.

Router R2 provides routing services for internal VLANs.

Two switches connect departmental workstations.

### Topology

ISP Router (R1)

↓

FortiGate Firewall

↓

Internal Router (R2)

↓

Switch Infrastructure

↓

Department Workstations

### Department Layout

| Department             | VLAN    | Device |
| ---------------------- | ------- | ------ |
| Human Resources        | VLAN 10 | PC1    |
| Information Technology | VLAN 20 | PC2    |
| Sales                  | VLAN 30 | PC3    |
| Finance                | VLAN 40 | PC4    |

---

## Project Objectives

* Design a segmented enterprise network.
* Implement VLAN-based departmental separation.
* Configure Inter-VLAN Routing.
* Deploy DHCP for automatic IP assignment.
* Integrate a FortiGate Firewall.
* Apply security policies and access controls.
* Verify network functionality through testing.
* Simulate enterprise security scenarios.

---

## Technologies Used

* GNS3
* Cisco IOS
* FortiGate Firewall
* VLANs
* Router-on-a-Stick
* DHCP
* IPv4 Networking
* Routing & Switching
* Network Security Policies

---

## VLAN Design

Each department was assigned a dedicated VLAN to improve security and reduce broadcast traffic.

| VLAN | Department | Subnet          |
| ---- | ---------- | --------------- |
| 10   | HR         | 192.168.10.0/24 |
| 20   | IT         | 192.168.20.0/24 |
| 30   | Sales      | 192.168.30.0/24 |
| 40   | Finance    | 192.168.40.0/24 |

Benefits:

* Network segmentation
* Better performance
* Enhanced security
* Simplified management

---

## Inter-VLAN Routing

Router R2 was configured using Router-on-a-Stick architecture.

Subinterfaces were created for each VLAN and configured as default gateways.

This allows communication between VLANs when permitted by security policies.

---

## DHCP Services

Dynamic Host Configuration Protocol (DHCP) was deployed to automatically provide:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server

Benefits:

* Reduced administrative effort
* Faster device deployment
* Consistent network configuration

---

## FortiGate Firewall Integration

The FortiGate Firewall was deployed between the ISP and internal network.

Security functions include:

* Traffic inspection
* Access control
* Security policy enforcement
* Network protection

---

## Security Policies

Implemented policies include:

### Allowed

* Internal users accessing the Internet
* IT department administrative traffic
* Approved business communications

### Denied

* Unauthorized inter-department traffic
* External access to internal hosts
* Unapproved services

These controls enforce the principle of least privilege.

---

## Testing & Validation

The following tests were performed:

### Connectivity Testing

* Host-to-host communication
* Gateway reachability
* Internet access verification

### DHCP Verification

* Automatic IP assignment
* Correct subnet allocation
* Gateway distribution

### Security Verification

* Firewall rule validation
* Traffic filtering checks
* VLAN isolation testing

### Troubleshooting Tools

* ping
* traceroute
* show ip route
* show vlan brief
* show ip interface brief
* FortiGate logs

---

## Skills Demonstrated

* Enterprise Network Design
* Cisco Routing & Switching
* VLAN Configuration
* Inter-VLAN Routing
* DHCP Deployment
* FortiGate Firewall Administration
* Network Security
* Access Control Implementation
* Network Troubleshooting
* Technical Documentation

---

## Project Outcome

Successfully designed and implemented a secure enterprise network featuring four departmental VLANs, dynamic IP address allocation, secure Internet connectivity, and firewall-enforced access control policies.

