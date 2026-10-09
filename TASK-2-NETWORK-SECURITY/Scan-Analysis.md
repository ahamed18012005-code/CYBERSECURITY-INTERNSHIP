# Task 2 - Network Scan Analysis

## Objective

To discover active hosts, identify open ports, and examine services running on the authorized laboratory target.

## Target Information

* Target Machine: Metasploitable 2
* Target IP: 192.168.100.20
* Network Range: 192.168.100.0/24
* Testing Machine: Kali Linux

## 1. Host Discovery

Command:
nmap -sn 192.168.100.0/24

Purpose:
To identify active hosts on the laboratory network without performing a port scan.

Observation:
The target at 192.168.100.20 was identified as active.

## 2. TCP SYN Scan

Command:
sudo nmap -sS 192.168.100.20

Purpose:
To examine TCP ports using SYN scanning.

## 3. UDP Scan

Command:
sudo nmap -sU 192.168.100.20

Purpose:
To investigate UDP services on the target.

## 4. Service-Version Detection

Command:
sudo nmap -sV 192.168.100.20

Purpose:
To identify services and attempt to determine their versions.

## 5. Operating-System Detection

Command:
sudo nmap -O 192.168.100.20

Purpose:
To estimate the target operating system using network responses.

## 6. Combined Scan

Command:
sudo nmap -sS -sV -O 192.168.100.20

Purpose:
To combine TCP SYN scanning, service-version detection, and operating-system detection.

## 7. Banner Grabbing

Command:
nc -nv 192.168.100.20 22

Purpose:
To connect to the SSH service and inspect the service banner or connection response.

## Observed Services

The assessment identified services including:

* FTP - Port 21
* SSH - Port 22
* Telnet - Port 23
* SMTP - Port 25
* DNS - Port 53
* HTTP - Port 80
* SMB/NetBIOS - Ports 139 and 445
* Additional RPC-related services

Approximately 977 closed TCP ports were reported in the scan documented in the report.

## Analysis

Exposed services increase the potential attack surface. Older service versions may require further investigation, but a service banner alone does not prove that a vulnerability is exploitable.

## Recommendations

* Disable services that are not required.
* Upgrade unsupported service versions.
* Restrict network access to necessary ports.
* Review scan results and investigate potential vulnerabilities.
* Repeat authorized scans after remediation.

## Ethical Consideration

All scanning activities were performed against the designated laboratory target for educational purposes.
