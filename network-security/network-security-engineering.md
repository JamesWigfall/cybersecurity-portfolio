# Enterprise Network Security Architecture

## Overview
This project demonstrates the design of a secure enterprise network architecture with a focus on segmentation, data loss prevention (DLP), and traffic monitoring.

## Architecture Highlights
- DMZ with web proxy and email servers
- Edge firewall protecting internal network
- VLAN segmentation for user and server environments
- Core switching infrastructure
- Data Loss Prevention (DLP) integration across multiple layers

## Security Components
- **Edge Firewall**: Filters inbound and outbound traffic
- **DLP Network Server**: Monitors network traffic for sensitive data
- **DLP Web Server**: Inspects outgoing web traffic
- **DLP Mail Server**: Scans outgoing email for data exfiltration
- **DLP Storage Server**: Indexes and protects sensitive data in storage systems
- **Endpoint DLP Agents**: Monitors desktops and laptops for data transfer risks

## Network Segmentation
- **DMZ**: Hosts externally exposed services (web, email)
- **Server VLAN**: Contains database and file servers
- **User VLANs**: Separates desktops and laptops from critical infrastructure

## Security Benefits
- Reduces attack surface through segmentation
- Improves visibility into data movement
- Enhances detection of insider threats
- Prevents unauthorized data exfiltration

## Diagram
![Network Architecture](../assets/network-diagram.png)
<img width="2048" height="921" alt="Assignment 4 - Network Diagram drawio" src="https://github.com/user-attachments/assets/74b00b49-0992-46fa-a3c4-2e32550a654c" />
