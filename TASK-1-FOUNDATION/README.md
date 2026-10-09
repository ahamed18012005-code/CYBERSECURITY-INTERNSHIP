# Task 1 - Foundation & Environment Setup

## Overview

Task 1 focused on cybersecurity fundamentals, Linux commands, lab environment setup, network connectivity, and introductory security tools.

## Lab Environment

* Attacker Machine: Kali Linux
* Target Machine: Metasploitable 2
* Virtualization Platform: Oracle VirtualBox
* Lab Network: cyberlab
* Kali Linux IP: 192.168.100.10
* Metasploitable 2 IP: 192.168.100.20

## Objectives

* Understand cybersecurity fundamentals.
* Set up a controlled virtual laboratory.
* Practice basic Linux commands.
* Verify connectivity between lab machines.
* Explore introductory network and security tools.

## Activities Performed

### 1. Virtual Lab Setup

Kali Linux and Metasploitable 2 were configured in Oracle VirtualBox for controlled security testing.

### 2. Network Configuration

The lab used an isolated internal network named cyberlab.

* Kali Linux: 192.168.100.10
* Metasploitable 2: 192.168.100.20

### 3. Connectivity Testing

The ping command was used to check connectivity between the two lab machines.

Command:
ping -c 4 192.168.100.20

Result: Connectivity to the target was verified.

### 4. Network Scanning

Nmap was used to identify open services on the target machine.

Command:
nmap 192.168.100.20

Services identified included FTP, SSH, Telnet, HTTP, MySQL, PostgreSQL, and VNC.

### 5. Network Traffic Analysis

Wireshark was explored to capture and inspect network packets. An ICMP filter was used during connectivity testing.

### 6. Web Security Tool

Burp Suite was launched and explored as an introductory web application security testing tool.

### 7. Netcat Testing

Netcat was used to check whether the target SSH port was reachable.

Command:
nc -zv 192.168.100.20 22

Result: SSH port 22 was reported open.

## Tools Used

* Kali Linux
* Oracle VirtualBox
* Metasploitable 2
* Nmap
* Wireshark
* Burp Suite
* Netcat
* Linux terminal

## Security and Ethics

All activities were conducted in a controlled laboratory environment using an intentionally vulnerable target for educational purposes.

Security testing should only be performed on systems for which authorization has been obtained.

## Conclusion

Task 1 provided foundational experience in setting up a virtual cybersecurity lab, using Linux commands, testing network connectivity, scanning services, and exploring network and web security tools.

## Deliverables

* TASK-1-REPORT.pdf
* Lab-Notes.md
* Linux-Cheat-Sheet.md
