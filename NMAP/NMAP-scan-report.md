# NMAP SCAN REPORT

## Objective:-
To identify active network services, open TCP/UDP ports, service versions, and operating system information of the authorized Metasploitable 2 test machine within the isolated Host-Only network.
## Target:-
Target IP: 192.168.19.4

Network: 192.168.19.0/24

Target: Metasploitable 2

## Tools:-

Kali Linux
Nmap

VirtualBox

Metasploitable 2

## TCP Scan:-

sudo nmap -sS 192.168.19.4

## UDP Scan:-

sudo nmap -sU 192.168.19.4

## Service & Version Detection:-

sudo nmap -sV 192.168.19.4

## OS Detection:-

sudo nmap -O 192.168.19.4

