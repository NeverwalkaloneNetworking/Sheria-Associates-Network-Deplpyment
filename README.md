# Sheria & Associates Law Firm - Network Deployment

## Project Overview
This project models a brand-new network infrastructure designed for **Sheria & Associates Law Firm**, located in Nairobi CBD. The firm required local file sharing, network printing, and secure high-speed internet access for 5 practicing lawyers.

## Topology Architecture
The infrastructure built inside Cisco Packet Tracer includes:
* **1x Cisco 2911 Edge Router** (`SHERIA-RTR`)
* **1x Cisco 2960 Core Switch**
* **5x Lawyer Workstations** (`PC1` through `PC5`)
* **1x Local File Server** (IP: `192.168.1.100`)
* **1x Network Printer** (IP: `192.168.1.200`)
* **1x Simulated ISP Infrastructure** (`ISP-Internet` Router & `8.8.8.8` External DNS Server)

## Core Technical Implementations
* **Subnetting & IP Addressing:** Configured a local private LAN (`192.168.1.0/24`) alongside a static public WAN point-to-point link (`203.0.113.0/30`).
* **Static Routing:** Established a Gateway of Last Resort (`0.0.0.0/0`) on the corporate edge pointing to the ISP gateway.
* **Network Address Translation (NAT):** Implemented NAT Overload (PAT) via Access Control Lists (ACL) to translate internal private IPs into a single routable public IP address (`203.0.113.1`).

## Verification & Testing
* Successfully validated internal file sharing and network printing via End-to-End ICMP Pings.
* Verified outbound internet connectivity by successfully pinging external resources (`8.8.8.8`).
