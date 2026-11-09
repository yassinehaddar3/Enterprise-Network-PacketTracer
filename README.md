# Enterprise Multi-Site Network Infrastructure 🏢🔌

## 📌 Project Overview
This project is a complete simulation of a medium-sized enterprise network infrastructure using Cisco Packet Tracer. It was designed to demonstrate practical networking skills in routing, switching, IP addressing, and network security.

## 🛠️ Technologies & Protocols Implemented
*   **VLANs & Trunking (802.1Q):** Network segmentation for IT, HR, Sales, and Servers.
*   **Inter-VLAN Routing:** Router-on-a-Stick configuration.
*   **Dynamic Routing (OSPF):** Site-to-site connectivity (Area 0) between HQ and Branch.
*   **DHCP Server:** Automated IP provisioning for all client devices.
*   **Internal Services:** DNS and HTTP Web Server configuration.
*   **Network Security (ACLs):** Extended Access Control Lists to restrict inter-departmental traffic (e.g., blocking Sales from accessing IT resources while allowing Web access).
*   **Device Security:** Console, VTY, and Privileged EXEC mode passwords.

## 🗺️ Network Topology
*(Insert Topology.png here)*

## 📝 IP Addressing Plan
| Site | VLAN / Network | Network Address | Default Gateway |
| :--- | :--- | :--- | :--- |
| HQ | VLAN 10 (IT) | 192.168.10.0 /24 | 192.168.10.1 |
| HQ | VLAN 20 (HR) | 192.168.20.0 /24 | 192.168.20.1 |
| HQ | VLAN 30 (Sales) | 192.168.30.0 /24 | 192.168.30.1 |
| HQ | VLAN 99 (Servers) | 192.168.99.0 /24 | 192.168.99.1 |
| Branch | VLAN 40 (Staff) | 192.168.40.0 /24 | 192.168.40.1 |
| WAN | Point-to-Point | 10.0.0.0 /30 | .1 (HQ) / .2 (Branch) |

## 🚀 How to Test
1. Download the `.pkt` file and open it in Cisco Packet Tracer.
2. PC clients will automatically request IPs via DHCP.
3. Test connectivity by navigating to `www.ista-hq.local` from the Branch PC.
4. Try pinging the IT department from the Sales PC to see the ACL drop the packets.
