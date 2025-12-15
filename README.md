# Intrusion Detection System (IDS) Network Design and Simulation

**Cisco Packet Tracer Project**

**Project Overview**

This project demonstrates the design and simulation of an Intrusion Detection System (IDS) within a multi-segment enterprise network using Cisco Packet Tracer. The IDS is integrated into the network to monitor traffic, detect suspicious activities, and enhance network security across multiple subnets.

The architecture reflects a real-world secure enterprise environment, combining routing, segmentation, centralized services, and traffic monitoring to identify potential intrusions.

**Project Objectives**

Design a secure enterprise network with multiple subnets

Integrate an Intrusion Detection System (IDS)

Monitor traffic between internal networks

Detect unauthorized access and suspicious ICMP activities

Improve visibility and security of network communications

**Tools & Technologies**

Cisco Packet Tracer

Cisco Routers (1941)

Cisco Switches (2960-24TT)

End Devices (PCs, Laptops, Smartphones)

Servers (FTP & Application Servers)

Printers

Wireless / Cellular Infrastructure

IDS Monitoring (Traffic inspection & alerting)

🌐 **Network Architecture**

The network consists of three monitored LAN segments, interconnected through routers where traffic passes through IDS-monitored links.

1️⃣ LAN 1 – User & Administration Network

Network: 192.168.1.0/24

Default Gateway: 192.168.1.1

Devices:

PCs (192.168.1.2 – 192.168.1.5)

Application Server (192.168.1.6)

Printer (192.168.1.7)

Switch: 2960-24TT

Security Focus: Internal user activity monitoring

2️⃣ LAN 2 – Core Services & IDS Monitoring Network

Network: 192.168.10.0/24

Default Gateway: 192.168.10.1

Devices:

PCs (192.168.10.2 – 192.168.10.5)

Laptop (192.168.10.6)

FTP Server (192.168.10.7)

Printer (192.168.10.8)

Switch: 2960-24TT

Security Focus: Server access monitoring & attack detection

3️⃣ LAN 3 – Wireless & External Access Network

Network: 192.168.30.0/24

Default Gateway: 192.168.30.1

Devices:

Laptop (192.168.30.2)

PC (192.168.30.3)

Smartphone (192.168.30.4)

Connectivity: Cell Tower (simulated external access)

Security Focus: Detection of unauthorized wireless access

🔐 **Intrusion Detection System (IDS) Design
IDS Placement**

Positioned on inter-router links

Monitors traffic between:

LAN 1 ↔ LAN 2

LAN 2 ↔ LAN 3

Focuses on north-south and east-west traffic

IDS Functions

Monitors ICMP, FTP, and general TCP/IP traffic

Detects:

Excessive ping requests (ICMP flood simulation)

Unauthorized access attempts

Suspicious cross-subnet communication

Generates alerts based on abnormal traffic patterns

🔁 Routing & Traffic Flow

Routers configured to enable full inter-subnet communication

All inter-LAN traffic traverses IDS-monitored paths

Central routing ensures visibility of attack vectors

**Testing & Simulation**
Normal Traffic Tests

ICMP ping between trusted hosts

FTP access to internal server

Printer access from authorized devices

Intrusion Simulation

Repeated ICMP requests from untrusted subnet

Cross-network scanning behavior

Unauthorized access attempts from wireless segment
**Testing NIDS & SYSLOG**
For our project we have used dynamic routing concept because it is more easy to use.
Another task for configuring this network was configuration of Servers i.e. Syslog, HTTP,
FTP. For Syslog server I have turned down all the service except logging service called
‘SYSLOG’ so that it can focus only to logging information come from IDS.
For configuring HTTP same concept like syslog. Here I made a custom webpage which can
be accessed from any host in the any network by IP address called 100.50.0.2
For configuring FTP same concept. Here I made a user called ‘harsh’ and password ‘123’
So now our entire network is configured properly.

Results

IDS successfully detects abnormal traffic patterns

Alerts observed during simulation mode in Packet Tracer

Difficulties
Setting up the IP address of all the systems in the network
Then we had Issue with Routing which was then tackled and solved using the concept
of Dynamic routing which enabled us to transfer files and packet from one system to
another.
Setting the protocols for http and ftp servers.
Having the command lines to work and prevent the intrusion with syslog.

⚙️ Key Security Features

Network segmentation using subnetting

Centralized traffic monitoring

Simulated intrusion detection

Visibility into internal and external traffic

Support for future IPS / firewall integration

📘 Learning Outcomes

Understanding IDS concepts and deployment

Network security monitoring

Traffic analysis and intrusion detection

Secure enterprise network design

Packet Tracer security simulation techniques

👤 **Author**

Patrick Phooko
Computer Scientist | Cybersecurity & Network Security Enthusiast
Lesotho 🇱🇸
