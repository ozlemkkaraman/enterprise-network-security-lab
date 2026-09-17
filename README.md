# Enterprise Network Security & Segmentation Lab

A network segmentation and access control lab designed and implemented using Cisco Packet Tracer.

## Overview

This project demonstrates a segmented enterprise network with separate VLANs for management, servers, users, DMZ, and guest devices.

The network uses router-on-a-stick inter-VLAN routing, DHCP, and extended ACLs to control communication between different network segments.

## Network Topology

The topology includes:

- Cisco 2911 Router
- Core Switch
- Management PC
- Server PC
- User PC
- DMZ Web Server
- Guest PC

## VLAN Configuration

| VLAN | Name | Network | Gateway |
|------|------|---------|---------|
| 10 | MANAGEMENT | 192.168.10.0/24 | 192.168.10.1 |
| 20 | SERVERS | 192.168.20.0/24 | 192.168.20.1 |
| 30 | USERS | 192.168.30.0/24 | 192.168.30.1 |
| 40 | DMZ | 192.168.40.0/24 | 192.168.40.1 |
| 50 | GUEST | 192.168.50.0/24 | 192.168.50.1 |

## Implemented Features

- VLAN creation and network segmentation
- Access and trunk port configuration
- 802.1Q router-on-a-stick inter-VLAN routing
- DHCP configuration
- Extended ACL configuration
- Guest network isolation
- DMZ web server
- HTTP and HTTPS services
- Access control between network segments

## Security Policies

- **Management VLAN:** Allowed to access network segments as required.
- **Server VLAN:** Provides access to required network resources.
- **User VLAN:** Allowed to access the Server VLAN and the DMZ web server through HTTP/HTTPS.
- **Guest VLAN:** Isolated from Management, Servers, Users, and DMZ networks.
- **DMZ:** Used to host the web server and separate the web service from internal network resources.

## Testing

The configured network and access control rules were tested in Cisco Packet Tracer.

| Test | Result |
|------|--------|
| User → DMZ HTTP | Allowed |
| User → DMZ HTTPS | Allowed |
| Guest → Management | Blocked |
| Guest → Servers | Blocked |
| Guest → Users | Blocked |
| Guest → DMZ | Blocked |
| Guest → Gateway | Allowed |

## Technologies

- Cisco Packet Tracer
- Cisco IOS
- VLAN
- 802.1Q
- Router-on-a-Stick
- DHCP
- Extended ACL
- IPv4
- HTTP / HTTPS

## Project Files

- `network-security-lab.zip` — Cisco Packet Tracer project file (`.pkt`) in ZIP format.

## Project Status

Completed as a Cisco Packet Tracer network segmentation and access control lab.

## Future Improvements

- Add a WAN/Internet connection and NAT
- Integrate a firewall appliance
- Add network monitoring and security logging
