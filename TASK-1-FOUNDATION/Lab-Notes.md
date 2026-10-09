# Task 1 - Lab Notes

## Objective

To establish a controlled cybersecurity laboratory and practice basic network discovery and security-tool usage.

## Lab Environment

* Virtualization: Oracle VirtualBox
* Attacker: Kali Linux
* Target: Metasploitable 2
* Internal Network: cyberlab

## Network Configuration

| Machine          | Interface | IP Address     |
| ---------------- | --------- | -------------- |
| Kali Linux       | eth1      | 192.168.100.10 |
| Metasploitable 2 | eth0      | 192.168.100.20 |

The Kali virtual machine also used a NAT adapter for external connectivity. The cyberlab internal network was used for communication with the target.

## 1. Connectivity Testing

Command:
ping -c 4 192.168.100.20

Observation:
The target responded to ping requests, confirming connectivity within the lab.

## 2. Nmap Scanning

Command:
nmap 192.168.100.20

Observation:
The scan identified services including FTP, SSH, Telnet, HTTP, MySQL, PostgreSQL, and VNC.

## 3. Wireshark

Wireshark was explored to capture and analyze network traffic.

An ICMP display filter was used to inspect packets related to connectivity testing.

## 4. Burp Suite

Burp Suite was launched and explored as an introductory web application security tool.

## 5. Netcat

Command:
nc -zv 192.168.100.20 22

Observation:
The target SSH port, 22, was reported open.

## Key Findings

* The two lab machines communicated over the internal network.
* Nmap identified multiple services on the target.
* Wireshark provided a way to inspect network packets.
* Netcat confirmed that the SSH port was reachable.
* Burp Suite was explored for web security testing.

## Conclusion

The lab introduced basic Linux networking, connectivity checks, service discovery, packet analysis, and security-tool usage.

## Ethical Consideration

All testing was performed in the controlled cyberlab environment against the intentionally vulnerable Metasploitable 2 machine.
