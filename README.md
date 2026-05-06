# Packet Tracer – Layer 3 Switch VLAN Lab

## Overview
Designed and configured a segmented network using a Layer 3 switch to enable inter-VLAN routing and centralized DHCP services.

This lab simulates an enterprise-style network with VLAN segmentation, routing between subnets, and automated IP address assignment.

---

## Technologies Used
- Cisco Packet Tracer
- VLANs
- Inter-VLAN Routing
- DHCP

---

## Lab Architecture
- Layer 3 Switch (routing + DHCP)
- VLAN 10 → 192.168.10.0/24
- VLAN 20 → 192.168.20.0/24
- Access ports assigned per VLAN
- Switch Virtual Interfaces (SVIs) used as default gateways

---

## Network Design

<img src="https://github.com/JonValladares/Packet-Tracer-layer-3-switch-lab/blob/98ae595fc141a41a33d8dcf0b0a5097eb6b897ac/diagrams/Network%20Diagram.png" alt="Network Topology" style="width:60%; height:auto;">

### VLAN 10 (LAN 1)
- Network: 192.168.10.0/24  
- Gateway: 192.168.10.1  
- Ports: Fa0/1–12  

### VLAN 20 (LAN 2)
- Network: 192.168.20.0/24  
- Gateway: 192.168.20.1  
- Ports: Fa0/13–24  

---

## Key Configurations
- Created VLANs and assigned switch ports  
- Configured SVIs for inter-VLAN routing  
- Enabled Layer 3 routing using `ip routing`  
- Configured DHCP pools for automatic IP assignment per VLAN  

---

## Verification

### DHCP Address Assignment (VLAN 10)
<img src="https://github.com/JonValladares/Packet-Tracer-layer-3-switch-lab/blob/98ae595fc141a41a33d8dcf0b0a5097eb6b897ac/Screenshots/ipconfigPC1.png" style="width:70%; height:auto;">


### DHCP Address Assignment (VLAN 20)
<img src="https://github.com/JonValladares/Packet-Tracer-layer-3-switch-lab/blob/d363040dc8e3e12a4d6a961aafecb4081b57c29f/Screenshots/ipconfigPC4.png" style="width:70%; height:auto;">

Devices received correct IP and gateway via DHCP  

---

### Routing Table (Layer 3 Switch)
<img src="https://github.com/JonValladares/Packet-Tracer-layer-3-switch-lab/blob/98ae595fc141a41a33d8dcf0b0a5097eb6b897ac/Screenshots/show_ip_route.png" style="width:70%; height:auto;">

Both VLAN networks are directly connected  

---

### Inter-VLAN Connectivity
<img src="https://github.com/JonValladares/Packet-Tracer-layer-3-switch-lab/blob/98ae595fc141a41a33d8dcf0b0a5097eb6b897ac/Screenshots/pingPC1toPC4.png" style="width:70%; height:auto;">

Successful communication between VLANs  

---

## Troubleshooting

**Issue:** Devices in different VLANs could not communicate  
**Cause:** Layer 3 routing was not enabled  
**Resolution:** Enabled `ip routing` on the switch  
**Result:** Restored inter-VLAN connectivity  

---

## Skills Demonstrated
- VLAN segmentation and switch configuration  
- Inter-VLAN routing using Layer 3 switching  
- DHCP configuration and IP management  
- Network troubleshooting and validation  
