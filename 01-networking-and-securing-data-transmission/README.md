# Project 1: Networking and Securing Data Transmission

## Project Overview
This project focused on designing a secure small-office network for TechCrush Technology Ltd, implementing network segmentation, controlling communication between departments, and examining secure data transmission.

This was a collaborative project completed as part of the TechCrush Cybersecurity Capstone, Cohort 8.

## Objectives
- Design and configure a departmental network.
- Implement VLAN segmentation.
- Apply Access Control Lists (ACLs) to restrict inter-department communication.
- Establish secure communication between Kali Linux and Ubuntu Server.
- Perform network reconnaissance and packet analysis.
- Demonstrate encrypted file transfer and data integrity verification.

## Tools and Technologies
- Cisco Packet Tracer
- Kali Linux
- Ubuntu Server
- Oracle VirtualBox
- Nmap
- Wireshark
- OpenSSH
- OpenSSL
- SCP
- SHA-256

## Activities Performed

### 1. Network Design and VLAN Configuration
Designed a small-office network using Cisco Packet Tracer, consisting of one router, two Cisco 2960 switches, eight PCs, and four departmental VLANs.

The VLAN configuration included:
- HR – VLAN 10
- Finance – VLAN 20
- IT – VLAN 30
- Sales – VLAN 40

Each department was assigned a separate subnet. Access Control Lists (ACLs) were configured to restrict communication between different VLANs.

### 2. Linux Environment and SSH Configuration
Configured Kali Linux and Ubuntu Server virtual machines in VirtualBox using a shared NAT network.

OpenSSH was enabled on Ubuntu Server to facilitate secure remote communication. Connectivity was tested using ping and SSH.

### 3. Network Reconnaissance
Used Nmap to identify the target host and examine exposed services. The scan identified SSH on TCP port 22 and reported the OpenSSH service version.

### 4. Packet Analysis
Used Wireshark to examine network traffic, including ICMP communication, SSH sessions, and Nmap scanning activity.

The analysis demonstrated the difference between visible ICMP traffic and encrypted SSH communication.

### 5. Secure Data Transmission
Explored SHA-256 hashing for data integrity verification, OpenSSL AES-256-CBC encryption, and SCP file transfer over SSH.

Packet analysis confirmed that the SCP/SSH communication was encrypted during transmission.

## Key Findings and Learning Outcomes
- Understood how VLANs support network segmentation.
- Learned how ACLs can restrict inter-department communication.
- Practised SSH configuration and secure remote access.
- Gained experience with Nmap reconnaissance and Wireshark packet analysis.
- Explored file encryption, hashing, and secure transfer.
- Improved understanding of network security controls and secure data transmission.

## Recommendations
- Use SSH key-based authentication.
- Keep OpenSSH and other network services updated.
- Restrict SSH access through firewall rules.
- Monitor network activity for suspicious scanning.
- Encrypt sensitive files before transmission.
- Verify file integrity using cryptographic hashes.

## Participation
This was a collaborative TechCrush Cybersecurity Capstone project. I actively participated in the project activities and practical exercises.

## Disclaimer
This project was completed for educational purposes in a controlled lab environment.