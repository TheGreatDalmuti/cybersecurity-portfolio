# TCP/UDP

TCP vs UDP Comparison (basics)
The two primary protocols at the transport layer are TCP and UDP.
A network application has to choose how to send its data. That choice comes down to reliable
or unreliable transmission.
Both reliable and unreliable have their benefits and drawbacks.

TCP Transmission Control Protocol
TCP is the most widely chosen option for transmitting data. This is because it can reliably send
and receive data.
The way TCP can provide such stable and reliable connections is in three ways .
1. Acknowledgements
2. Sequencing
3. Checksum
Before any of that can happen, first we need to start a reliable connection.
TCP does this by using what's called a threeway handshake.
1. SYN
2. SYN-ACK
3. ACK
Data is not sent all in one piece

UDP(User Datagram Protocol) has none of the error handling, sequencing or reliability of TCP.
UDP is fast and rapid.
TCP offers great connection and reliability, it comes at a price or resource and latency.
UDP is very useful in a situation when we need live, real-time connections. For example, voice
calls, video calls, and gaming all need fast real-time connections

# OSI Model

The OSI model (or Open System Interconnection Model) is an absolute fundamental model
used in networking. This critical model provides a framework for dictation how all networked
devices will send.
One of the main benefits of the OSI model is that devices can have different functions and
designs on a network while communicating with other devices.
Data sent across a network that follows the uniformity of the OSI model can be understood by
other devices.
The OSI model consists of seven layers which are illustrated in the diagram below. Each layer
has a different set of responsibilities and is arranged from Layer 7 to Layer 1.

7. Application
6. Presentation
5. Session
4. Transport
3. Network
2. Data link
1. Physical

Layer 7: Application
The application layer of the OSI model is the layer that you will be most familiar with. This is
because the application layer is the layer in which protocols and rules are in place to determine
how the user should interact with data sent or received.
Everyday applications such as email clients, browsers, or file server browsing such as FileZilla
provide a friendly, Graphical User Interface (GUI) for users to interact with data sent or received.
Other protocols include DNS( Domain Name System), which is how website addresses are
translated into IP addresses.

Layer 6: Presentation
Layer 6 of the OSI model is the layer in which standardisation starts to take place . Software
developers can develop any software such as an email client differently, the data still needs to
be handled in the same way - no matter how the software works.
This layer acts as a translator for data to and from the application layer (layer 7). The receiving
computer will also understand data sent to a computer in one format destined for in another
format. For example, when you send an email, the other user may have another email client to
you, but the contents of the email will still need to display the same.
Security features such as data encryption (like HTTPS when visiting a secure site) occur at this
layer.

Layer 5 : Session
Once data has been correctly translated or formatted from the presentation layer (layer 6), the
session layer (layer 5) will begin to create a connection to the other computer that the data is
destined for. When a connection is established, a session is created. While this connection is
active , so is the session.
The session layer synchronises the two computers to ensure that they are on the same page
before data is sent and received. Once these checks are good, the session layer will begin to
divide up the data sent into smaller chunks of data and begin to send the chinks one at a time.

Layer 4 : Transport
Layer 4 of the OSI model follows two protocols
TCP
UDP

Advantages of TCP
Guarantees the accuracy of data/
Capable of synchronising two devices to prevent each other from being flooded with data.
Performs a lot more processes for reliability.

Disadvantages of TCP
Requires a reliable connection between the two devices. If one small chunk of data is not
received then the entire chunk of data cannot be used/
A slow connection can bottleneck another device as the connection will be reserved on the
receiving computer the whole time
TCP is significantly slower than UDP because more work has to be done by devices using this
protocol.

Advantages of UDP
UDP is much faster than TCP
UDP leaves the application layer to decide if there is any control over how quickly packets are
sent.
UDP does not reserve a continuous connection on a device as TCP does.

Disadvantages of UDP
UDP doesn't care if the data is received
It is quite flexible to software developers in this sense.
This means that unstable connections result in a terrible experience for the user.

Layer 3 : Network
OSPF(Open Shortest Path First) and RIP (Routing Information Protocol).
These factors that decide what routes is taken is decided by the following:
What path is the shortest ? has the least amount of devices that the packet needs to travel
across.
What path is the most reliable ?"
Which path has the faster physical connection?
At this layer, everything is dealt with via IP addresses such as 192.168.1.100. Devices such as
routers capable of delivering packets using IP addresses are known as Layer 3 devices -
because they are capable of working at the third layer of the OSI Model.

Layer 2 : Data Link
The data link layer focuses on the physical addressing of the transmission. It receives a packet
from the network layer and adds in the physical MAC( Media Access Control) address of the
receiving endpoint. Inside every network enabled computer is a Network Interface Card (NIC)
which comes with a unique MAC address to identify it.
MAC addresses are set by the manufacturer and are physically burnt into the card

Layer 1 : Physical
The layer references the physical components of the hardware used in networking and is the
lowest layer that you will find

# Packets & Frames

Packets and frames are small pieces of data that, when forming together, make a large piece of
information or message. They are two different things in the OSI model
A frame is at layer 2- the data link layer, meaning there is no such information as IP addresses.
Putting an envelope within an envelope and sending it away.
This process is called encapsulation . At this stage, when talking about IP addresses, we are
talking about packets. When the encapsulating information is stripped away, we're talking about
the frame itself.
Packets are an efficient way of communicating data across networked devices. The data is
exchanged in small pieces, there is less chance of bottleneck occurring across a network than
large messages being sent at once.
Packets have different structures that are dependent upon the type of packet that is being sent.

Example of the Internet Protocol
A packet using this protocol will have a set of headers that contain additional pieces of
information to the data that is being sent across a network
Source Address : The IP address of the device that the pack is being sent from so that the data
knows where to return to.
Destination Address : The device's IP address the packet is being sent to so that the data
knows where to travel next.

TCP packets contain various sections of information known as headers that are added
Header Description
Source Port The value is the port opened by the sender to send the TCP packet from. This
value is chosen randomly .
Destination Port this value is the port number that an application or service is running on the
remote host; for example a webserver running on port 80. Unlike the source port , this value is
not chosen at random
Sequence Number When a connection occurs. The first piece of data transmitted is given a
random number.
Checksum This value is what gives TCP integrity. A mathematical calculation is made where
the output is remembered. When the receiving device performs the mathematical calculation,
the data must be corrupt if the output is different from what was sent.
Data This header is where the data bytes of a file is being transmitted, is stored
Flag This header determines how the packet should be handled by either device during the
handshake process. Specific flags will determine specific behaviors, which is what we'll come on
to explain below.

Three-Way handshake - the term given for the process used to establish a connection between
two devices. The Three-way handshake communities using a few special messages

SYN A SYN message is the initial packet sent by a client during the handshake. This packet
is used to initiate a connection and synchronise the two devices together (Utilizes Sequence
Numbers)
SYN/ ACK This packet is sent by the receiving device to acknowledge the synchronisation
attempt from the client.
ACK The acknowledgement packet can be used by either the client or server to acknowledge
that a series of messages/ packets have been successfully received.
DATA Once a connection has been established, data is sent via the "DATA" message.
FIN This packet is used to cleanly close the connection after it has been completed.
RST This packet abruptly ends all communication. This is the last resort and indicates there
was some problem during the process.

UDP/IP
UDP packets are much simpler than TCP packets and have fewer headers. However, both
protocols share some standard headers
Time to Live This field sets an expiry timer for the packet, so it doesn't clog up your network if it
never manages to reach a host or escape.
Source address The IP address of the device that the packet is being sent from, so that data
knows where to return to
Destination Address The deceive's IP address the packet is being sent to so that data knows
where to travel next
Source Port This value is the port that is opened by the sender to send the UDP pocket form.
This value is randomly chosen : for example, a webserver running on port 80, Unlike the source
port, this value is not chosen at random.
Data This header is where data, i.e. bytes of a file that is being transmitted, is stored.

UDP is stateless

# Extending Your Network

Port Forwarding
Port forwarding is an essential component in connecting applications and services to the
internet. Without port forwarding, applications and services such as web servers are only
available to devices within the same direct network.

Firewalls 101
A firewall is a device within a network responsible for determining what traffic is allowed to enter
and exit. An administrator can configure a firewall to permit or deny traffic from entering or
exiting a network based on numerous factors
Firewalls perform packet inspection
Firewalls come in all shapes and sizes. From dedicated pieces of hardware that can handle a
magnitude of data to residential routers or software such as Snort, firewalls can be categorised
into 2 to 5 categories

Firewall Category Description
Stateful this type of firewall uses the entire information from a connection; rather than
inspecting an individual packet, this firewall determines the behaviour of a device based upon
the entire connection.
This firewall type consumes many resources in comparison to stateless firewalls as the decision
making is dynamic.
If a connection from a host is bad, it will block the entire device

Stateless This firewall type uses a static set of rules to determine whether or not individual
packets are acceptable or not . For example, a device is sending a bad packet will not
necessarily mean the entire device is then blocked
Whilst these firewalls use much fewer resources than alternatives, they are much less
sophisticated.
Firewall type is great when receiving large amounts of traffic from a set host

VPN Basics
A Virtual Private Network is a technology that allows devices on separate networks to
communicate securely by creating a dedicated path between each other over the Internet .
Devices connected within this tunnel form their own private network.

VPN Protocols
PPP This technology is used by PPTP to allow for authentication and provide encryption of
data. VPNs work by using a private key and public certificate. A private key & certificate must
match for you to connect .
This technology is not capable of leaving a network by itself.

PPTP The Point to Point Tunneling Protocol is the technology that allows the data from PPP
to travel and leave a network.
PPTP is very easy to set up and is supported by most devices. Weakly encrypted in comparison
to alternatives

IPSec Internet Protocol Security encrypts data using the existing Internet PProtocol
framework.
Difficult to set up
Strong encryption and is also supported on many devices.

Routers operate at layer 3 of the OSI model
A switch is a dedicated networking device responsible for providing a means of connecting to
multiple devices. Switches can facilitate many devices using Ethernet Cables
Switches can operate at both layer 2 and layer 3 of the OSI model. These are exclusive in the
sense that layer 2 switches can operate at layer 3.
Layer 3 switches are more sophisticated than layer 2, as they can perform some of the
responsibilities of a router. Namely, these switches will send frames to devices and route
packets to other devices using the IP protocol

VLAN (Virtual Local Area Network) allows specific devices within a network to be virtually split
up. This network separation provides security because it means that rules in place determine
how specific devices communicate with each other.
