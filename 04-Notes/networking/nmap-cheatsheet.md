# Kali Linux Tools

NMAP
Network scanning - Technique for identifying "devices"
1. These devices have IPs & MAC addresses
2. IP addresses have TCP/UDP ports (1-65,535)
3. Ports are open (listening), closed (No service around the port), filtered (firewall, router, or
security appliance actively blocks connection attempts, unfiltered (reachable and
accessible)
4. Ports run OS & Services

Common Ports
21 FTP 135 RPC
22 SSH 139 SMB (old)
23 Telnet 143 IMAP4
25 SMTP 161 SNMP
53 DNS 162 SNMP traps
80 HTTP 389 LDAP
88 Kerberos 443 HTTPS
110 POP3 445 SMB
111 NIX 3389 RDP

# NMAP

● Free, Powerful Network Discovery tool
● IP/Host/Port scanning
● Services discovery
● OS detection
● Version Detection
● Scriptable interaction with targets (NSE)
● Info on targets, including reverse DNS names, device types, and MAC addresses
● Reconnaissance & Info Gathering

Syntax
● Nmap [Scan Types] [Options] <target>

Target Options
192.168.0.1 Single IP
dan.host.me Single Host
192.168.1.0/24 Entire subnet
dan.host.me/24 Entire subnet
192.168.1.* Entire subnet
192.168.1.19-50 IP Range
192.168.1.10-50, 11.56 Multiple targets

Nmap help menu ( nmap -h)

Basic Scan Options 1
-h nmap help
-sP Hosts up
-sS TCP SYN Scan (half-open)
-sT TCP Complete Scan
-Pn No Ping
-sV get service version
-sU UDP Scan
-sL Lists Targets
-sA Test for Firewall Protection
(Open,filtered, unfiltered Ports)

Basic Scan Options 2
-r No random
–top-ports Top Ports
-6 IPV6
-il <file> Input File
-oA/-X/-oN… <file>
–exclude Exclude from scan
-n Don't resolve name
-R Reverse DNS lookup
-F Fast Mode

Basic Scan Options 3
-O OS Detection
-A OS/Service/script/traceroute
–version-intensity <level> Light to all probes (0-9)
-sC All default Scripts
-v,-vv Verbosity levels
-PR ARP
-sn No Port
-PS <port list. Specified ports

When port scanning with Nmap, there are three basic scan types. These are:
-TCP connect scans (-sT)
-SYN Scans (-sS)
-UDP Scans(-sU)

Less common
-TCP Null Scans (-sN)
-TCP FIN Scans (-sF)
-TCP Xmas Scans (-sX)

NSE Scripts
The Nmap Scripting Engine is a powerful addition to Nmap, extending its functionality quite
considerably. NSE Scripts are written in the Lua programming language, and can be used to do
a variety of things: from scanning for vulnerabilities, to automating exploits for them.

A full list of scripts and their corresponding arguments
- https://nmap.org/nsedoc/
Or
- /usr/share/nmap/scripts

Wireshark
Metasploit

Must Do
● Launch an exploit
● Open Wireshark in your lab and:
1. Start a capture on your active network interface.
2. Open a web browser and visit a website
3. Stop the capture.
4. Filter for
Dns
Tcp
http
