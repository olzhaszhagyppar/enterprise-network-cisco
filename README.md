# Multi-Site Enterprise Network Simulation

An individual university project developed in Cisco Packet Tracer for the Networking and Communication module at Coventry University Kazakhstan.

The project simulates a corporate network connecting two branches in **Astana and Almaty**, with departmental network segmentation, dynamic routing, and gateway redundancy.

## Network Architecture

- Two geographically separated sites with routers, switches, servers, wireless access points, and end devices.
- Department-based VLAN segmentation and IP subnetting.
- Inter-VLAN routing using IEEE 802.1Q.
- OSPF dynamic routing.
- HSRP gateway redundancy.
- DHCP address pools and relay configuration.
- Multiple ISP connections represented in the topology.

## Technologies Used

| Technology | Implementation |
|---|---|
| Cisco Packet Tracer | Network design and simulation |
| OSPF | Dynamic routing and route exchange |
| HSRP | Redundant virtual gateways |
| VLAN / 802.1Q | Department segmentation and inter-VLAN routing |
| DHCP | Address allocation and relay configuration |
| TCP/IP | IPv4 addressing and subnetting |

## Configuration Details

Four VLANs were configured on the inspected Astana router.

| VLAN | Subnet | Virtual Gateway |
|---|---|---|
| 10 | 172.16.98.0/26 | 172.16.98.62 |
| 20 | 172.16.98.64/26 | 172.16.98.126 |
| 30 | 172.16.98.128/26 | 172.16.98.190 |
| 40 | 172.16.98.192/26 | 172.16.98.254 |

## Verification

Cisco CLI outputs confirmed:

- Five OSPF neighbor entries in FULL state.
- OSPF-learned routes in the routing table.
- Four active HSRP groups with standby peers.

End-to-end connectivity, DHCP lease allocation, and automatic failover have not yet been fully verified.

## Project File

[Download the Cisco Packet Tracer simulation](Olzhas%20epn.pkt)

Open the `.pkt` file using Cisco Packet Tracer to inspect the network topology and device configurations.

## About

This network was independently designed and configured as an individual university assignment. It is a simulated environment, not a production network.
