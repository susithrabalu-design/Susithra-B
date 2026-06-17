NETWORK SECURITY ASSESSMENT REPORT

INTRODUCTION

Network security is a critical aspect of information technology that focuses on protecting computer networks, devices, and data from unauthorized access, cyberattacks, and other security threats. As organizations and individuals increasingly rely on networked systems for communication and data exchange, ensuring the security and reliability of these networks has become essential.

A network security assessment is a systematic process used to evaluate the security posture of a network by identifying active hosts, open ports, running services, and potential vulnerabilities. Such assessments help organizations understand their exposure to security risks and implement appropriate measures to strengthen their defenses.

In this project, a network security assessment was conducted using Nmap and Wireshark. Nmap was utilized to scan the network and identify devices, open ports, and services, while Wireshark was used to capture and analyze network traffic. The collected data was examined to detect possible security weaknesses and evaluate the overall security status of the network.

The findings of this assessment provide valuable insights into network behavior, potential vulnerabilities, and recommended security improvements. By identifying risks and suggesting corrective measures, this assessment contributes to enhancing the confidentiality, integrity, and availability of network resources.

OBJECTIVE

The objective of this project is to assess the security of a local network using network scanning and traffic analysis tools. The assessment helps identify active hosts, open ports, running services, and potential security vulnerabilities. Nmap is used for network scanning, while Wireshark is used to monitor and analyze network traffic.

TOOLS USED 

Nmap

 (Network Mapper) is an open-source tool used to discover devices, services, and open ports on a network.

 Wireshark

 Wireshark is a network protocol analyzer used to capture and inspect packets traveling across a network

 OPERATING systeM 

 Windows 10 / Windows 11

 METHODOLOGY

 The network security assessment was conducted in three phases

 Phase 1: Network Scanning

The local network was scanned using Nmap to identify active devices and open ports.

Command Used:

nmap -sV 192.168.1.0/24

The command performs service version detection and identifies active hosts on the network.

Phase 2: Traffic Capture

Wireshark was used to capture network packets for a period of 5 minutes.

Steps:

Open Wireshark.
Select the active network interface.
Start packet capture.
Generate normal internet traffic.
Stop the capture and save the file.

Phase 3: Analysis

The captured packets and scan results were analyzed to identify:

Open ports
Active services
Network protocols
Potential vulnerabilities

NMAP SCAN RESULTS 

Host Information

IP Address	Status	Open Ports
192.168.1.1	Active	80, 443
192.168.1.5	Active	135, 445
192.168.1.10	Active	22

Open Ports Identified

Port	Service	Risk Level
22	SSH	Medium
80	HTTP	Medium
443	HTTPS	Low
135	RPC	Medium
445	SMB	High

WIRESHARK ANALYSIS 

Protocol Distribution
Protocol	Purpose
TCP	Reliable communication
UDP	Fast communication
DNS	Domain name resolution
HTTP	Web traffic
HTTPS	Secure web traffic

OBSERVATION

Majority of traffic was HTTPS encrypted traffic.
DNS requests were observed for website access.
TCP handshake packets were captured successfully.
No suspicious packet flooding was detected.

SECURITY VULNERABILITIES IDENTIFIED 

Vulnerability 1: Open SMB Port (445)

Risk:
Unauthorized users may attempt access through SMB services.

Recommendation:
Disable SMB if not required and update the operating system regularly.

Vulnerability 2: Multiple Open Ports

Risk:
Open ports increase the attack surface.

Recommendation:
Close unused ports and services.

Vulnerability 3: Unencrypted HTTP Traffic

Risk:
Data transmitted through HTTP can be intercepted.

Recommendation:
Use HTTPS instead of HTTP whenever possible.

RECOMMENDATION 

Enable firewall protection.
Close unnecessary ports.
Use strong passwords.
Keep systems updated.
Implement HTTPS for secure communication.
Regularly monitor network traffic.
Perform periodic vulnerability assessments.

CONCLUSION 

The network security assessment successfully identified active devices, open ports, and network traffic patterns. Nmap provided valuable information regarding services running on the network, while Wireshark helped analyze packet-level communication. Several potential security concerns were identified, and appropriate recommendations were provided to improve the overall security posture of the network.

REFERENCES 

Nmap Documentation
Wireshark Documentation
Cyber Security Best Practices
Network Security Fundamentals


