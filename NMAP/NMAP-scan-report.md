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


## Findings:-

| port | Protocol | State | Service | Version |
|---|---|---|---|---|
| `21` | tcp | `open` | ftp |Vsftpd 2.3.4 |
| `22` | tcp | `open` | ssh |OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0) |
| `23` | tcp | `open` | telnet | Linux telnetd |
| `25` | tcp | `open` | smtp |Postfix smtpd |
| `53` | tcp | `open` | domain |ISC BIND 9.4.2 |
| `80` | tcp | `open` | http |Apache httpd 2.2.8 ((Ubuntu) DAV/2) |
| `111` | tcp | `open` | rpcbind |2 (RPC #100000) |
| `139` | tcp | `open` | netbios-ssn |samba smbd 3.X 4.X (workgroup: WORKGROUP) |
| `445` | tcp | `open` | netbios-ssn |Samba smbd 3.X - 4.X (workgroup: WORKGROUP) | 
| `512` | tcp | `open` | exec |netkit-rsh rexecd |
| `513` | tcp | `open` | login? | |
| `514` | tcp | `open` | shell |Netkit rshd |
| `1099` | tcp | `open` | java-rmi | GNU Classpath grmiregistry |
| `1524` | tcp | `open` | bindshell |Metasploitable root shel |
| `2049` | tcp | `open` | nfs |2-4 (RPC #100003) |
| `2121` | tcp | `open` | ftp |ProFTPD 1.3.1 |
| `3306` | tcp | `open` | mysql |MySQL 5.0.51a-3ubuntu5 |
| `5432` | tcp | `open` | postgresql |PostgreSQL DB 8.3.0 - 8.3.7 | 
| `5900` | tcp | `open` | vnc |VNC (protocol 3.3) |



