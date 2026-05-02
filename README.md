\# Cyber Security Internship - Task 1



\## Scan Your Local Network for Open Ports



\---



\## Objective



To discover open ports on devices in the local network and understand network exposure using Nmap.



\---



\## Tools Used



\* Nmap

\* Wireshark (Optional)



\---



\## Local Network Information



\* \*\*IPv4 Address:\*\* 10.25.73.57

\* \*\*Subnet Mask:\*\* 255.255.255.0

\* \*\*Network Range:\*\* 10.25.73.0/24



\---



\## Command Used



```bash

nmap -sS 10.25.73.0/24

```



\---



\## Scan Results



\### Active Hosts Found



| IP Address   | Open Ports                                      | Service           |

| ------------ | ----------------------------------------------- | ----------------- |

| 10.25.73.167 | 53                                              | DNS               |

| 10.25.73.57  | 80, 135, 139, 445, 3306, 4343, 4449, 5357, 7070 | Multiple Services |



\---



\## Port Analysis



\### Router / Gateway (10.25.73.167)



\* \*\*53/tcp\*\* → DNS Service



\### Local Machine (10.25.73.57)



\* \*\*80/tcp\*\* → HTTP

\* \*\*135/tcp\*\* → MSRPC

\* \*\*139/tcp\*\* → NetBIOS

\* \*\*445/tcp\*\* → SMB / Microsoft-DS

\* \*\*3306/tcp\*\* → MySQL

\* \*\*4343/tcp\*\* → Unicall

\* \*\*4449/tcp\*\* → PrivateWire

\* \*\*5357/tcp\*\* → WSDAPI

\* \*\*7070/tcp\*\* → RealServer



\---



\## Security Risks Identified



\* Open SMB ports may expose file sharing vulnerabilities

\* Open MySQL port may expose database access

\* Open HTTP service may reveal web applications

\* Unnecessary open ports increase attack surface



\---



\## Interview Questions \& Answers



\### 1. What is an open port?



An open port is a network port actively accepting incoming connections.



\### 2. How does Nmap perform a TCP SYN scan?



Nmap sends SYN packets and analyzes responses:



\* SYN-ACK = Open

\* RST = Closed



\### 3. What risks are associated with open ports?



Unauthorized access, exploitation of services, information leakage.



\### 4. Difference between TCP and UDP scanning?



TCP scans use connection/SYN packets; UDP scans send UDP packets and wait for responses.



\### 5. How can open ports be secured?



Close unused ports, use firewalls, restrict access, keep services updated.



\### 6. What is a firewall's role regarding ports?



It allows or blocks traffic based on configured port/security rules.



\### 7. What is a port scan and why do attackers perform it?



A port scan identifies open services and vulnerabilities for reconnaissance.



\### 8. How does Wireshark complement port scanning?



It captures/analyzes packets to inspect scan traffic and responses.



\---



\## Outcome



\* Learned basic network reconnaissance

\* Understood TCP SYN scanning

\* Identified exposed services in local network

\* Analyzed potential security risks



\---



\## Files Included



\* README.md

\* scan\_results.txt



\---



