# The CIA Triad

Confidentiality
Ensuring digital information is not available to unauthorized individuals.
Integrity
Ensuring digital information is not modified without permission
Availability
Ensuring digital information is not unavailable when needed.

# Encryption

Asymmetric encryption solves the problem of key distribution
Symmetric encryption handles the heavy lifting because it's way faster

# Vulnerabilities

● A weakness in a system
Allows the bad guys to gain access or cause a security breach
● Many different vulnerability types
Data Injection
Broken authentication process
Sensitive data
Security misconfiguration

# DAD

● Disclosure is the opposite of confidentiality. In other words, disclosure of confidential
data would be an attack on confidentiality.
● Alteration is the opposite of integrity. For example, the integrity of a cheque is
indispensable
● Destruction/ Denial is the opposite of Availability
The opposite of the CIA Triad would be the DAD Triad: Disclosure, Alteration, and Destruction.

# Exploits

● Take advantage of a vulnerability
Gain control of a system
Modify data
Disable a Service

A zero-day attack occurs when hackers exploit a previously unknown software or hardware
vulnerability before the developer is aware of it or can issue a patch

Open permissions
● Very easy to leave a door open
● Increasingly common with cloud storage

Unsecured root accounts
● The Linux root account
The Administrator or superuser account
● Disable direct login to the root account
Use the su or sudo option
● Protect accounts with root or administrator access

Error messages can provide useful information to an attacker
● Service type, version information , debug data

Weak Encryption
● Encryption Protocol (AES, 3DES, etc.)
Length of the encryption key (40 bits, 128 bits, 256 bits, etc.)
Hash used for the integrity check (SHA, MD5,etc.)
Wireless encryption (WEP,WPA)
● Some cipher suites are easier to break than others
● TLS is one of the most common issues
Over 300 cipher suites
● Which are good and which are bad?
Weak or null encryption(less than 128 bit key sizes), outdated hashes (MD5)

Insecure Protocols
● Some protocols aren't encrypted
All traffic sent in the clear
Telnet, FTP, SMTP, IMAP
● Verify with a packet capture
View everything sent over the network
Change it to an encrypted protocol
● Use the encrypted versions
SSH,SFTP, IMAPS, etc.

Default settings
● Every application and network device has a default login
● Mirai botnet
Takes advantage of default configurations
60+ default configuration
Cameras, routers, doorbells, garage door openers, etc

Open ports and services
● Services will open ports
● Often managed with a firewall
Manage Traffic flows
● Firewall rulesets can be complex
It's easy to make a mistake
● Always test and audit
Double and Triple check

Legacy platforms
● Some devices remain installed for a long time
● Legacy devices
Older operation systems, applications, middleware
● May bee running end of life software
The risk needs to be compared to return

# Phases of Ethical Hacking

Identify the tools hackers might utilize during each phase

● Reconnaissance (Recon)
First phase
Also Known as Footprinting (or) Information Gathering
Hacker gathers information as much as possible
3 Groups
1. People involved
2. Host
3. Network
Active Footprinting —----> Hacker directly interact with the target
Passive Footprinting —---> Hacker will indirectly interact with the target

● Scanning
Second Phase
Attacker starts scanning for vulnerabilities / weaknesses
With the help of information gathered in phase 1
1. Port scanning —---> Attacks scan the Target system for available ports
2. Vulnerability scanning —-----> attacker scans the target to find weaknesses
within the system.
3. Network Scanning —--> Attacker scans the target to find the network firewalls etc

● Gaining access
Attacker makes use of information gathered from Phase 1 & 2 to gain access of a Target
Attacks will be performed
> Phishing Attacks
> DoS attacks
> Website Attacks
> ETC

● Maintaining Access
How long Attackker gains access for future exploitations
Hacker maintains access until they complete his/ her activities.

Clearing tracks
> Attacker clears all his/her activities
> Attacker Clears logs, applications, data, etc.

● Clearing Traps

● Reports (Only for Ethical Hacking)
Report with completed process need to be submitted

Directory enumeration is the process of discovering hidden directories and files on
a web server that aren't linked from the website but still exist.

# Fundamental Concepts of Security Models

The utilization of security models directly answer questions about how to upload Confidentiality,
Integrity, and Availability
Three foundational security models:

● Bell-LaPadula Model
Claims to achieve confidentiality by specifying three rules
1. Simple Security Property : This property is referred to as "no read up"; it states
that a subject at a lower security level cannot read an object at a higher security
level. This rule prevents access to sensitive information above the authorized
level.
2. Star Security Property: this property is referred to as "no write down"; it states
that a subject at a higher security level cannot write to an object at a lower
security level. This rule prevents the disclosure of sensitive information to a
subject of lower security level.
3. Discretionary-Security Property: This property uses ann access matrix to allow
read and write operations. An example access matrix is shown in the table below
and used in conjunction with the first two properties.

Subjects Object A Object B
Subject 1 Write No access
Subject 2 Read/Write Read

● The Biba Integrity Model
The Biba Model aims to achieve integrity by specifying two main rules:
1. Simple Integrity Property: This property is referred to as "no read down"; a higher
integrity subject should not read from a lower integrity object
2. Star Integrity Property : This property is referred to as "no write up"; a lower
integrity subject should not write to a higher integrity object.

● The Clark Wilson Model
The Clark-Wilson model also aims to achieve integrity by using the following concepts:
Constrained Data Item (CDI) : This refers to the data type whose integrity we want to
preserve.
Unconstrained Data Item (UDI) : This refers to all data types beyond CDI, such as
user and system input.
Transformation Procedures (TPs) : These procedures are programmed operations,
such as read and write, and should maintain the integrity of CDIs.
Integrity Verification Procedures (IVPs) : These procedures check and ensure the
validity of CDIs.

5 design principles
1. Least Privilege —> Give users only the permissions they need
2. Attack Surface Minimization —--> Disable or remove unnecessary services/
features
3. Centralized Parameter Validation —> Check all user input in one place.
4. Centralized General Security Services —-> Keep security functions( like
authentication) centralized.
5. Preparing for Error and Exception Handling —> Fail safely and don't leak
sensitive information in errors.

# Order of Learning

Pre Security
Linux Fundamentals
Networking
Junior Penetration Tester
Beginner CTFs alongside it
