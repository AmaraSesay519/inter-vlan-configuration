# Inter-VLAN Communication Configuration Using Cisco Packet Tracer

##  Project Overview

This project demonstrates the configuration and implementation of Inter-VLAN communication using Cisco Packet Tracer. The network was designed using routers, switches, and VLANs to enable communication between different VLANs through Inter-VLAN routing using the Router-on-a-Stick method.

The project showcases practical networking skills including VLAN creation, trunk configuration, IP addressing, and network segmentation.



#  Author

**Amara Sesay**



#  Objectives

* Configure VLANs on switches.
* Assign switch ports to different VLANs.
* Configure Inter-VLAN routing.
* Enable communication between multiple VLANs.
* Understand VLAN segmentation and routing concepts.



#  Tools & Technologies Used

* Cisco Packet Tracer
* Routers
* Switches
* VLANs (Virtual Local Area Networks)
* Ethernet Cables
* Networking Protocols



#  Network Design

The network topology consists of:

* One Router
* One or More Switches
* Multiple PCs connected to different VLANs

Each VLAN represents a separate logical network, while the router enables communication between the VLANs.



#  VLAN Configuration

| VLAN ID | VLAN Name      |
| ------- | -------------- |
| 10      | COMPUTER-SCIENCE |
| 20      | LAW      |
| 30      | AGRIC          |



#  Configuration Steps

## Switch VLAN Configuration

```bash
Switch(config)# vlan 10
Switch(config-vlan)# name COMPUTER-SCIENC

Switch(config)# vlan 20
Switch(config-vlan)# name LAW

Switch(config)# vlan 30
Switch(config-vlan)# name AGRIC
```



## Assigning Ports to VLANs

```bash
Switch(config)# interface fastEthernet0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10
```



## Router Inter-VLAN Configuration

```bash
Router(config)# interface g0/0.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# ip address 192.168.10.1 255.255.255.0

Router(config)# interface g0/0.20
Router(config-subif)# encapsulation dot1Q 20
Router(config-subif)# ip address 192.168.20.1 255.255.255.0
```



# Testing & Verification

* Successful communication within the same VLAN.
* Successful communication between different VLANs.
* Ping tests verified proper Inter-VLAN routing.
* Network segmentation was achieved successfully.



#  Features

* VLAN Creation and Management
* Inter-VLAN Communication
* Router-on-a-Stick Configuration
* Network Segmentation
* Practical Cisco Networking Simulation



#  Benefits of the Project

* Improved understanding of VLAN concepts.
* Enhanced practical networking skills.
* Better knowledge of routing and switching.
* Experience with Cisco Packet Tracer simulations.



#  Future Improvements

* Implement DHCP Services
* Add Access Control Lists (ACLs)
* Improve Network Security
* Expand the Network Topology
* Add Wireless VLAN Support



#  References

* Cisco Networking Academy
* Cisco Packet Tracer Documentation
* VLAN & Inter-VLAN Routing Concepts



#  Conclusion

This project successfully demonstrates the implementation of Inter-VLAN communication using Cisco Packet Tracer. VLANs were configured effectively, and communication between different VLANs was achieved through proper router and switch configuration.

The project provided valuable hands-on experience in routing, switching, VLAN management, and enterprise network design.
