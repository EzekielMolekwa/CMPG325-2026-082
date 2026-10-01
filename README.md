# CMPG325-2026-082

## CMPG325 Computer Networks – Individual Semester Project

**Student:** Molekwa, ER  
**Student Number:** 45618070  
**Project ID:** CMPG325-2026-082  
**Client ID:** CLI-082  
**Organisation:** Ramokoka & Partners Attorneys (Vryburg)  
**Industry:** Legal Services  
**Allocated IP Address Block:** 172.30.52.0/23  
**Networking Challenge:** Access Control Lists (ACLs) – Traffic Filtering Policy  

## Project Overview

This repository serves as a record of the planning, network design, configuration, implementation, testing and supporting documentation developed for the CMPG325 Computer Networks individual semester project.

The project focuses on designing and simulating a network solution for Ramokoka & Partners Attorneys in Vryburg using Cisco Packet Tracer. The proposed network provides wired connectivity for internal users, wireless connectivity within designated public areas, VLAN-based network segmentation, inter-VLAN routing, DHCP services and controlled communication between network segments through Access Control Lists (ACLs).

The design also considers Change Request CR6, which requires provision for a future branch office. Address space is reserved for this future expansion without constructing or implementing a second network site within the current project.

## Project Progress

### Milestone 1 – Client Design Review
- [x] Client Requirements Analysis
- [x] Physical Network Topology
- [x] Logical Network Topology
- [x] IP Addressing Plan
- [x] Initial GitHub Repository

### Milestone 2 – Network Implementation and Testing
- [x] Build Network in Cisco Packet Tracer
- [x] Configure VLANs
- [x] Configure IP Addressing
- [x] Configure Inter-VLAN Routing
- [x] Configure DHCP Services
- [x] Configure Public Wireless Network
- [x] Implement ACL Traffic Filtering
- [x] Perform Network Connectivity Tests
- [x] Verify ACL Operation
- [x] Record Testing Evidence
- [x] Document Troubleshooting Activities

### Final Project Submission
- [ ] Final Cisco Packet Tracer File
- [ ] Final Technical Documentation
- [ ] Complete Network Testing Evidence
- [ ] Completed GitHub Project Portfolio
- [ ] Project Demonstration Video

## Repository Structure

- `Milestone_1/` – Contains the client requirements, physical and logical topology designs, and IP addressing documentation.
- `Packet_Tracer/` – Contains Cisco Packet Tracer network simulation files.
- `Configuration/` – Contains configuration records and supporting network configuration evidence.
- `Testing/` – Contains connectivity tests, ACL verification and other network testing evidence.
- `Screenshots/` – Contains screenshots collected during network implementation, configuration and testing.

## Current Status

Milestone 1 has been completed, including the client requirements analysis, physical topology, logical topology and IP addressing plan.

Milestone 2 implementation is in progress. The Cisco Packet Tracer network has been built and configured with VLAN segmentation, inter-VLAN routing, static addressing, DHCP services, public wireless access and ACL-based traffic filtering. Connectivity and ACL testing has also been performed, with evidence collected in the repository.

The ACL traffic-filtering policy was tested using the public wireless network. Traffic from the public Wi-Fi network to protected internal VLANs was denied, while permitted traffic to an external routed destination was successfully allowed. The corresponding configuration and testing evidence is stored in the repository.

Further final verification, documentation and submission preparation remain before the project is considered complete.
