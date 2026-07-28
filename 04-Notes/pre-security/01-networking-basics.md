# Networking Basics

## IP addresses
Internet Protocol address
The router gives devices the specified IP address
Unique numerical assigned to each device connected to a computer network that uses the
internet protocol for communication
Identifying the host or network interface and providing the location of the host in the network
The address allows devices to locate and communicate with each other on a network, enabling
data exchange between devices.

Types of IP Addresses
IPv4 192.168.1.1
32 - bit
4.3 billion unique addresses

IPv6
2001:db8:00:1234:0:567:8:1
128-bit
340 undecillion addresses

## DNS
Domain Name System (alternative to an ip address) Domain name Maximum Length 253
So instead of remembering 104.26.10.229, you can remember tryhackme.com instead.

Domain Hierarchy
Root Domain > Top-Level Domains > Second-Level Domains

Top-Level Domain
Two types of TLD. gTLD (Generic Top Level) and ccTLD ( Country Code Top Level Domain). 63
character limit

Second-Level Domain
Taking tryhackme.com as an example, the .com part is the TLD, and tryhackme is the Second
Level Domain. 63 character limit

Subdomain
A subdomain sits on the left-hand side of the Second-Level Domain using a period to separate
it; for example, in the name admin.tryhackme.com the "admin" part is the subdomain.

DNS Record Types

A Record
These records resolve to IPv4 addresses, for example 104.26.10.229

AAAA Record
These records resolve to IPv6, for example 2606:4700:20::681a:be5

CNAME Record
These records resolve to another domain name, for example, TryHackMe's online shop has the
subdomain name store.tryhackme.com which returns a CNAME record shops.shopify.com .
Another DNS request would then be made to shops.shopify.com to work out the IP address

MX Record
These records resolve to the address of the servers that handle the email for the domain you
are querying, for example an MX record response for tryhackme.com would look like
alt1.aspmx.l.google.com. Perfect for if the main server goes down and email needs to be sent to
a backup server

TXT Record
TXT records are free text fields where any text-based data can be stored. TXT records have
multiple uses, but some common ones can be to list servers that have authority to send an
email on behalf of the domain.

Making A Request
1. When you request a domain name, your computer first checks its local cache to see if
you've previously looked up the address recently; if not, a request to your Recursive
DNS Server will be made .
2. A recursive DNS Server is usually provided by your Internet Server Provider, but you can
also choose your own. This server also has a local cache of recently looked up domain
names. If a result is found locally, this is sent back to your computer, and your request
ends here. If the request cannot be found locally, a journey begins to find the correct
answer.
3. The root servers act as the DNS backbone of the internet; their job is to redirect you to
the correct Top Level Domain Server, depending on your request. If , for example, you
request www.tryhackme.com, the root server will recognise the Top Level Domain of
.com and refer you to the correct TLD server that deals with .com addresses.
4. The TLD server holds records for where to find the authoritative server to answer the
DNS request. The authoritative server is often also known as the nameserver for the
domain. For example, the name server for tryhackme.com is kip.ns.cloudflare.com and
uma.ns.cloudflare.com
5. An authoritative DNS server is the server that is responsible for storing the DNs records
for a particular domain name and where any updates to your domain name DNS records
would be made. Depending on the record type, the DNS record is then sent back to the
Recursive DNS Server, whereas local copy will be cached for future requests and then
relayed back to the original client that made the request. DNS records all come with a
TTL value. This value is a number represented in seconds that the response should be
saved for locally until you have to look it up again. Caching saves on having to make a
DNS request every time you communicate with a server.

## Routers
Connect us to the internet
Connects networks
The person giving data pings for the network including ip addresses sends out packets
to anyone when ip is known asking for who is that given ip then ping is given.
When trying to connect on layer 2 to a device outside of the network the message is sent
over and over and rejected each time.
You have to added a router between two different networks
You must know the mac address so that the switch can send to the router
Routers are layer 3 devices that can handle the ip address
Router does not know the the destinations layer 2 address so how does he find out
Another arc message asking where is the arc message
Sends the arc message to the other network
once the arc is received and confirmed
Switch > mac addresses layer 2
Router > addresses layer 3
Router has a pathway to other networks and the internet

## Ports
A port is not a physical connection
It's a logical connection that's used by programs and services to exchange information
It specifically determines which program or service on a computer or server that is going
to be used
Ports will have a unique number that will identify them
0-65535
A port number is always associated with an IP address.
If you want to connect to the internet > An Ip address determines the location of that
server.
A port number determines which service or program on that server it wants to use.
(whether it be a web page, FTP, Email, So on…)
A very common port that most people use every day is port 80
Port 80 is associated with HTTP (Hypertext Transfer Protocol), which is web pages
So for example if you access google.com (IP Address) 215.114.85.17:80 (port number)
To see this information you can use Netstat Network Statistics
Command line tool that is used to display the current network connections and port
activity on your computer.
FTP (File Transfer Protocol) is the standard protocol used to transfer files over a network
FTP uses port number 21
Port numbers are broken down into 3 categories
Port Numbers 0-1023 are called System or Well-Known ports.
Port Numbers 1024-49151 are called User or Registered ports
These are ports that can be registered by companies and developers for a particular
service
Port numbers 49152-65535 are called Dynamic or Private Ports.
These are client-side ports that are free to use
These are ports that your computer assigns temporarily to itself during a session
Example When viewing a web page.

## LAN
Local Area Network (LAN) Topologies
A LAN is, as the name implies, a local network. This network could be as small as two
computers that are connected to each or or large, with up to thousands of devices connect
The main premise of a star topology is that devices are individually connected via a central
networking device such as a switch or hub.
Any information sent to a device in this topology is sent via the central device to which it
connects.
When using connections for external resources we utilized WAN (Wide Area Network) in order
to connect to other remote LANs or servers on the internet.
On a local area network, we utilize one dominant protocol called Ethernet

1. SOHO LAN
The SOHO (Small Office Home Offices) LAN is utilized for your home internet network for
connectivity and perhaps to share some files between computers.
Wireless networking is also based on standards that are published by the IEEE. Everything that
is wireless related starts with 802.11.
For Wireless connectivity, we add an access point to our network. This allows the wired and
wireless devices to communicate with each other. If you want to leave your LAN and
communicate with the outside world, you will need a router.
The router uses Ethernet for connectivity with your local network. On the WAN side, it uses
another technology like DSL, cable, satellite, 4G/LTE to communicate with the Internet provider.

2. Enterprise LAN
Enterprises typically use the same technology as SOHO LANs but on a larger scale.
There might be hundreds or thousands of devices connected to the network that are
located in one or multiple buildings.

3. Conclusion
LANs (Local Area Network) use Ethernet as the primary technology for wired
connectivity. Some of the network devices we use on our LAN are switches, access
points, and routers. Ethernet is the dominant standard that is used on our LAN, wireless
devices use another standard.
