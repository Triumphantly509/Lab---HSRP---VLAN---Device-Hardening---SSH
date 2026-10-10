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

## Codes / Commands

- Create all the vlans on both switches
- assign ip addresses to the device management vlan
- Switch 0
  <div>
    <img width="635" height="496" alt="image" src="https://github.com/user-attachments/assets/4104bf44-ca52-4148-a39f-62e9e287f908" />
  </div>
- Configuring SSH device managements and allow only managers (Vlan 30) to access the devices.
- Encrypting passwords in the configuration, and creates authentication credentials for administrative access.
<div>
  <img width="386" height="58" alt="image" src="https://github.com/user-attachments/assets/04c4f651-9916-4143-add2-e0f7763eca7b" />
</div>
- Configure the domain name
<div>
  <img width="432" height="312" alt="image" src="https://github.com/user-attachments/assets/f5b1b3cc-d592-4aac-bd4b-abac8487c5fe" />
</div>
- Assigns Ip address to the remote switch.
<div>
    <img width="627" height="374" alt="image" src="https://github.com/user-attachments/assets/166bbc8b-d65a-4f69-bb9f-c14178bf75ea" />
  </div>
- Create an Access list to the managers vlan to access the management devices.
<div>
  <img width="500" height="142" alt="image" src="https://github.com/user-attachments/assets/ca3d428b-35d4-465c-93e9-f12b422cfc37" />
</div>
- line console 0
<div>
  <img width="397" height="331" alt="image" src="https://github.com/user-attachments/assets/9d639701-98b9-4f99-a1bc-615850ea3632" />
</div>
- SSH
<div>
  <img width="476" height="259" alt="image" src="https://github.com/user-attachments/assets/2ff52a1a-39ec-47d2-8621-8a4d0e9846c2" />
</div>


## FLOATING STATIC ROUTE 

<div>
  <img width="1444" height="636" alt="image" src="https://github.com/user-attachments/assets/e640aaa3-0e01-4829-8019-69c8ce27c8d1" />
</div>



## DYNAMIC ROUTING RIP, OSPF EIGRP 

<div>
  <img width="1049" height="659" alt="image" src="https://github.com/user-attachments/assets/475a13c2-51b7-4065-9a04-78f184e5649d" />
</div>
