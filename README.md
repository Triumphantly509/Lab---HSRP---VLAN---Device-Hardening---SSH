# Lab---HSRP---VLAN---Device-Hardening---SSH

<div>
  <img width="1246" height="675" alt="image" src="https://github.com/user-attachments/assets/74ccd835-ab3e-4d5e-b3d1-25bceda24bf2" />
</div>

- HQ VLAN REQ. 

- VLAN 10 - STAFF (192.168.10.0/24)
- VLAN 20 - VOICE (192.168.20.0/24)
- VLAN 30 - Managers (192.168.30.0/24)
- VLAN 40 - Device Management (192.168.40.0/28)
- VLAN 99 - NATIVE 
- VLAN 999 - BLACKHOLE for Unused Ports

- SECURITY REQUIREMENT
1. Segment Network According to VLANs
2. Configure Basic Device Hardening on all Network Devies (Routers and Switches) - Privilege and console passwords, use SSH for remote communication and only the Device Management VLAN should be able to access routers and switches remotely (Idea - Use Access-Lists to Control SSH)
3. Configure Trunks Between Switches to use the Native VLAN 99 and allow only Used VLANs on Trunks
4. Move All Unsed Ports to the BLACK HOLE VLAN 999 and Shutdown
5. Create Local account for SSH mangement 

- Redundancy Requriement

1. Configure Etherchannel on links between switches
2. Conifgure HSRP on Routers for Redundancy 
 
- Routing Req
Configure Static Route Between HQ-Edge and Router 0 and Router 1
Configure Default Route Between HQ-Edge and Branch  
 
- GOAL 
Acheive communication between PCs in HQ and BRANCH PC
Acheive communication between PCs in HQ
