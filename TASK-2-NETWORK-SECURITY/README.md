# Task 2 - Network Security & Scanning

## Overview

Task 2 focused on network reconnaissance, host discovery, service enumeration, vulnerability assessment, packet analysis, and basic firewall concepts in a controlled cybersecurity laboratory.

## Lab Environment

* Testing Machine: Kali Linux
* Target Machine: Metasploitable 2
* Target IP Address: 192.168.100.20
* Lab Network: 192.168.100.0/24

## Objectives

* Understand passive and active reconnaissance.
* Identify active hosts and open ports.
* Detect service versions and operating-system information.
* Explore vulnerability assessment tools.
* Analyze network traffic using Wireshark.
* Understand SYN flood concepts and firewall rules.
* Recommend appropriate security controls.

## Activities Performed

### 1. Reconnaissance

Studied reconnaissance techniques, including:

* WHOIS
* NSLookup
* Google Dorking
* Shodan
* Ping sweep
* Banner grabbing

### 2. Host Discovery

Command:
nmap -sn 192.168.100.0/24

The command was used to discover active hosts on the laboratory network.

### 3. Port and Service Scanning

The following Nmap techniques were explored:

* TCP SYN scanning
* UDP scanning
* Service-version detection
* Operating-system detection
* Combined scanning

Example commands:
sudo nmap -sS 192.168.100.20
sudo nmap -sU 192.168.100.20
sudo nmap -sV 192.168.100.20
sudo nmap -O 192.168.100.20
sudo nmap -sS -sV -O 192.168.100.20

### 4. Banner Grabbing

Command:
nc -nv 192.168.100.20 22

Netcat was used to examine the target SSH service.

### 5. Vulnerability Assessment

OpenVAS/Greenbone was explored for vulnerability assessment and identification of potential security weaknesses.

### 6. Network Traffic Analysis

Wireshark was used to study protocols and traffic including:

* HTTP
* FTP
* DNS
* TCP
* UDP
* ARP
* ICMP

### 7. SYN Flood Concepts

The SYN flood technique was studied in a controlled lab context to understand how excessive connection requests can affect service availability.

### 8. Firewall Concepts

Linux iptables rules were studied to understand packet filtering and network traffic control.

## Key Findings

* The target was discovered on the laboratory network.
* Multiple services were identified, including FTP, SSH, Telnet, SMTP, DNS, HTTP, SMB/NetBIOS, and related services.
* Service-version and operating-system detection provided additional assessment information.
* Vulnerability assessment and packet analysis helped identify areas requiring further review.
* Firewall rules can help restrict unwanted network traffic.

## Security Recommendations

* Disable unnecessary services.
* Upgrade outdated software.
* Restrict exposed ports using firewall rules.
* Review service versions and investigate potential vulnerabilities.
* Monitor network traffic for suspicious activity.
* Apply security updates regularly.
* Perform scans only on authorized systems.

## Ethical Considerations

All practical testing was performed in a controlled laboratory environment for educational purposes.

Reconnaissance, scanning, and vulnerability assessment should only be conducted on systems for which explicit authorization has been obtained.

## Conclusion

Task 2 provided practical experience in reconnaissance, host discovery, port scanning, service detection, vulnerability assessment, packet analysis, and firewall concepts.

The exercises highlighted the importance of identifying exposed services, reviewing potential weaknesses, and applying appropriate security controls.

## Deliverables

* TASK-2-REPORT.pdf
* Scan-Analysis.md
* Vulnerability-Analysis.md
