# Packet-Tracer-layer-3-switch-lab
Configuring multple LANs using a layer 3 swit with inter-VLAN routing

**Technologies Used**
<ul>
  <li>Cisco Packet Tracer</li>
  <li>VLANs</li>
  <li>Inter-VLAN Routing</li>
  <li>DHCP Configuration</li>
</ul>

**Network Design**
<ul>
  <li>VLAN 10: 192.168.10.0/24</li>
  <li>VLAN 20: 192.168.20.0/24</li>
  <li>Layer 3 switch used as gateway and DHCP server</li>  
</ul>

**Key Configurations**
<ul>
  <li>Created VLANs and assigned switch ports</li>
  <li>Configured SVIs for routing between VLANs</li>
  <li>Enabled ip routing</li>
  <li>Configured DHCP pools for automatic IP assignment</li>
</ul>

**Verification**
<ul>
  <li>Devices successfully received IP addresses via DHCP</li>
  <li>Inter-VLAN communication verified using ping command</li>
</ul> 

**Troubleshooting**

When I first configured the network I assigned static IPs to verify communication between SVIs but didn't receieve a response across VLANs. After reviewing the configuration and  researching the issue, I found the cause. I never enabled `ip routing`. After enabling it I verified inter-VLANs connectivity via ping command.