# network-security-scanning
## Objective
The objective of this task was to perform
reconnaissance, network scanning, vulnerability
assessment, packet analysis and firewall testing
in an isolated cybersecurity lab.

## Lab Environment
Attacker: Kali Linux

Target:Metasploitable 2

Network: VirtualBox Host-only Adapter

Target IP:192.168.19.4

## Tools Used

- WHOIS
- NSLookup
- Nmap
- Netcat
- OpenVAS/GVM
- Wireshark
- hping3
- iptables

## 1. Reconnaissance

WHOIS is a query and response protocol used to retrieve registration details about a domain name or IP address block, such as owner contact information, registrar details, domain creation/expiration dates, and authoritative nameservers.

NSLOOKUP (Name Server Lookup) is a command-line network administration tool used to query Domain Name System (DNS) servers to obtain domain name or IP address mappings (such as A records, MX records, or PTR records).

## 2. Host Discovery

Ping Sweep is a network discovery technique used to determine which IP addresses in a target range are online and active. It sends ICMP Echo Request packets (or TCP/UDP probes) to multiple IP addresses in parallel; hosts that are powered on and reachable respond with ICMP Echo Replies, allowing an analyst to map live targets before scanning.

## 3. Port Scanning

TCP Scans: Connect to target TCP ports to identify open services.

TCP SYN Scan (-sS): Sends a SYN packet. If the port responds with SYN-ACK, the port is open (half-open scanning without completing the 3-way handshake).

UDP Scans (-sU): Send UDP packets to target UDP ports. If the port returns an ICMP "Destination Unreachable / Port Unreachable" message, the port is closed. If no response is received (or a UDP response is returned), Nmap marks the port as open|filtered.

## 4. Service Detection

The -sV flag in Nmap enables Service and Version Detection. After identifying open ports, Nmap probes those specific ports using a database of service signatures to determine the exact software application name and version number running on each port (e.g., Apache httpd 2.2.8 or ProFTPD 1.3.1).

## 5. OS Detection

The -O flag in Nmap enables Operating System Detection. Nmap sends a series of TCP, UDP, and ICMP packets to open and closed ports on the target machine, inspecting subtle differences in how the target's TCP/IP stack responds (such as TCP window size, initial sequence numbers, and IP ID fields) to fingerprint the OS version.

## 6. Vulnerability Assessment

OpenVAS (Greenbone Security Assistant) performs automated vulnerability scans by running Network Vulnerability Tests (NVTs) against target hosts. Findings are categorized by CVSS (Common Vulnerability Scoring System) severity scores ranging from Low to Critical. Reports detail security flaws, affected ports, CVE references, and recommended vendor mitigations.

## 7. Packet Analysis

Packet analysis using tools like Wireshark inspects raw network traffic across different protocols:

1. HTTP: Captures unencrypted web traffic on port 80, revealing cleartext GET/POST requests, URIs, headers, user-agents, and HTML response content.

2. FTP: Captures unencrypted file transfer traffic on port 21, allowing analysts to extract plain-text authentication credentials (USER and PASS commands) and data streams.

3. DNS: Captures domain resolution traffic on UDP port 53, showing client queries for domain names and server responses containing IP mapping records.

## 8. SYN Flood Simulation

A SYN Flood Simulation is a controlled Denial of Service (DoS) test performed in an isolated lab environment using tools like hping3 (e.g., sudo hping3 -S -p 80 -c 20 192.168.19.4). The attacker sends a rapid sequence of TCP SYN requests to a target port without completing the 3-way handshake, exhausting the server's connection queue resources to test detection and firewall response capabilities.

## 9. Firewall

iptables is a command-line firewall utility in Linux that uses policy chains to inspect and filter network traffic.

## 10. Security Findings


## 12. Conclusion

The assessment demonstrated how reconnaissance,
network scanning, vulnerability assessment,
packet analysis and firewall controls can be used
to identify and understand network security risks
within an authorized laboratory environment.
