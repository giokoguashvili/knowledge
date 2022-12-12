# OSI model
![OSI model](https://user-images.githubusercontent.com/8178412/149652541-3e79634d-9691-4491-9999-af23a99089c9.png)


# Networking
```
Application     | L7 |              |                       |                   | HTTP/FTP/WS           | DNS/Telnet                            |
Presentation    | L6 |              |                       |                   | SSL/TLS               |                                       |
Session         | L5 | Sync         | Data                  |                   |                       |                                       |
Transport       | L4 | Connection   | Segments/Datagram     |                   | TCP/UDP               |                                       |
Network         | L3 | Routing      | Packets               | Router            | IP                    | ICMP/IPSec/BGP/RIP/OSPF               |
Data-Link       | L2 | Adressing    | Frames                | Switch/Bridge     | MAC/LLC/IMEI          | ARP                                   | IEEE802.11/IEEE802.3
Physical        | L1 | Send Signals | Bits                  | Hub/NIC/Cable     |                       |                                       | Ethernet

Physical Layer
    Cabling
        Coaxial Cable
        Twisted Cable
        Fiber Optic Cable

        CAT 5/6/7 

        Half-Duplex
        Full-Duplex
        RJ-45 Port
        SFP Port
    Devices
        Bridge
        Hub
        Switch
        Router
        
Data Link
        NIC     - Network Interface Controller  (RJ-45), Network Interface Card, Adapter, LAN Adapter, Wireless NIC, Wired/Wireless
        MAC     - Medium Access Control
        LLC     - Logical Link Control
        IMEI    - International Mobile Equipment Identifier 

Network Topology
    Bus 
    Ring
    Star
    Mesh
    Tree
    Hybrid


IP Adresses
    Unicast
    Multicast
    Broadcast

OSI                     - Open Systems Interconnection Model

IEEE                    - Network Protocols
                            802.3   LAN   Ethernet 
                            802.11  WLAN                    
RFC                     - Internet Protocols
W3C                     - Web Standarts

WAN                     - Wide Area Network
LAN                     - Local Area Network
VLAN                    - Virtual LAN
VPN                     - Virtual Private Network
DMVPN                   - Dynamic Multipoint VPN
SSL VPN                 - Secure Sockets Layer Virtual Private Network
IPsec                   - IP Security
GRE                     - Generic Routing Encapsulation

PAT                     - Port Address Translation
NAT                     - Network Address Translation
DNAT                    - Destination Network Address Translation (External (untrusted) to Internal (trusted))
                          translates destination IP address generally when connecting from public IP address to private IP address
SNAT                    - Secure Network Address Translation (Internal (trusted) to External (untrusted))
                          translates source IP address generally when connecting 
                            private IP address to public IP address
SSH                     - Secure Shell
Telnet                  - an application protocol used on the WAN or LAN to provide a bidirectional interactive text-oriented communication facility using a virtual terminal connection
ISP                     - Internet Service Provider

Firewall        
Socket      
Gateway     
```

- [Internet protocol suite](https://en.wikipedia.org/wiki/Internet_protocol_suite) - wiki
- [TCP / IP protocol stack - reference map](https://informatics.buzdo.com/specific/tcp-ip-1.htm)

# Protocol Stack
![Protocol Stack](https://user-images.githubusercontent.com/8178412/149652519-946df1e8-56ce-483e-bf52-626b6e760546.png)
![Protocol Stack](https://user-images.githubusercontent.com/8178412/149652522-120953df-3e69-4b83-804a-350cf7fa61d5.gif)

```
Data Link Layer
    ARP (IPv4)          - Address Resolution Protocol 
                          The Address Resolution Protocol is a communication protocol used for discovering the link layer address, such as a MAC address, 
                          associated with a given internet layer address, typically an IPv4 address
                          
    NDP (IPv6)          - Neighbor Discovery Protocol

Network Layer   
    IP (IPv4/v6)        - Internet Protocol version 4/6
    
    DHCP                - Dynamic Host Configuration Protocol
                          Dynamic Host Configuration Protocol (DHCP) is a client/server protocol that automatically provides an Internet Protocol (IP) host 
                          with its IP address and other related configuration information such as the subnet mask and default gateway.
                          
    STP                 - Spanning Tree Protocol 
                          The Spanning Tree Protocol (STP) is a network protocol that builds a loop-free logical topology for Ethernet networks.
                          The basic function of STP is to prevent bridge loops and the broadcast radiation that results from them.

    ICMP                - Internet Control Message Protocol (ping)

Routing Protocols                          

    RIP                 - Routing Information Protocol
                        The Routing Information Protocol (RIP) uses a single routing metric to measure the distance between the source and the destination network.
                        Each hop in a path from the source to the destination is assigned a hop-count value, which is typically 1.
    OSPF                - Open Shortest Path First
    BGP                 - Border Gateway Protocol
    
    IGMP                - Internet Group Management Protocol
    EIGRP               - Enhanced Interior Gateway Routing Protocol


Transport Layer 
    TCP                 - Transmission Control Protocol
    UDP                 - User Datagram Protocol
    RUDP                - Reliable UDP

Session Layer   
    DNS                 - Domain Name System
    NetBIOS / IP        - Network Basic Input/Output System over IP for TCP / IP Environment

Application Layer   
    HTTP                - Hypertext Transfer Protocol
    FTP                 - File Transfer Protocol 
    WSS                 - Web Sockets 
    SMTP                - Simple Mail Transfer Protocol 
    TELNET              - TCP / IP Terminal Emulation Protocol
    NTP                 - Network Time Protocol

Security    
    IPSec               - Internet Protocol Security
    SSL                 - Secure Sockets Layer
    TLS	                - Transport Layer Security Protocol

Ports:  
    FTP                 - 20 - Data, 21 - Control
    SSH                 - 22
    TELNET              - 23
    SMTP                - 25
    DNS                 - 53
    DHCP                - 67, 68
    HTTP                - 80
    POP3                - 110
    NTP                 - 123
    IMAP                - 143
    BGP                 - 179
    IMAP                - 143
    HTTPS/SSL           - 443
    UDP                 - 1900
    RDP                 - 3389
    SSDP                - 1900
    
Other
    SSDP - Simple Service Discovery Protocol
```

### Protocols

- WebRTC
- ICE/STUN/TURN
- WebSocket
- WebTransport
- HTTP3
- QUIC
- Homa
- gRPC
- DRPC
- Protobuf
- Server-Sent Event
- TCP
- UDP
- Direct Sockets API (Raw Socket API)

### [Routing Protocols](https://en.wikipedia.org/wiki/Routing_protocol)
- [IGP - Interior Gateway Protocol](https://en.wikipedia.org/wiki/Interior_gateway_protocol)
used for exchanging routing table information between gateways (commonly routers) within an autonomous system (for example, a system of corporate local area networks). This routing information can then be used to route network-layer protocols like IP
    - [**RIP** - Routing Information Protocol](https://en.wikipedia.org/wiki/Routing_Information_Protocol) <br/>
    s one of the oldest distance-vector routing protocols which employs the hop count as a routing metric. RIP prevents routing loops by implementing a limit on the number of hops allowed in a path from source to destination

    - [**OSPF** - Open Shortest Path First](https://en.wikipedia.org/wiki/Open_Shortest_Path_First) <br/>
    is a routing protocol for Internet Protocol (IP) networks. It uses a link state routing (LSR) algorithm and falls into the group of interior gateway protocols (IGPs), operating within a single autonomous system (AS)

    - **IS-IS**
    
    - [**IGRP** - Internet Group Management Protocol](https://en.wikipedia.org/wiki/Interior_Gateway_Routing_Protocol) <br/>
    was created in part to overcome the limitations of RIP (maximum hop count of only 15, and a single routing metric) when used within large networks

    - [**EIGRP** - Enhanced Interior Gateway Routing Protocol](https://en.wikipedia.org/wiki/Enhanced_Interior_Gateway_Routing_Protocol) <br/>
    is an enhanced distance vector protocol that uses Diffusing Update Algorithm (DUAL) for shortest path calculation
- [EGP - Exterior Gateway Protocol](https://en.wikipedia.org/wiki/Exterior_Gateway_Protocol) - a routing protocol used to connect different autonomous systems on the Internet
    - [**BGP** - Border Gateway Protocol](https://en.wikipedia.org/wiki/Border_Gateway_Protocol) <br/>
    is classified as a path-vector routing protocol, and it makes routing decisions based on paths, network policies, or rule-sets configured by a network administrator

![Routing protocol classification computer networks](https://upload.wikimedia.org/wikipedia/commons/4/47/Computer_Network_Routing_Protocol_Classification_-en.png)


## TCP

- [Flow Control](https://en.wikipedia.org/wiki/Flow_control_(data)) <br/>
    is the process of managing the rate of data transmission between two nodes to prevent a fast sender from overwhelming a slow receiver


- [Congestion Control & Avoidance](https://en.wikipedia.org/wiki/Network_congestion) <br/>
    Networks use congestion control and congestion avoidance techniques to try to avoid collapse
- [MTU - Maximum Transmission Unit](https://en.wikipedia.org/wiki/Maximum_transmission_unit) <br/>
    is a term used in networking and operating systems. It defines the largest size of the packet that can be transmitted as a single entity in a network connection. The size of the MTU dictates the amount of data that can be transmitted in bytes over a network. 
- [MSS - Maximum Segment Size](https://en.wikipedia.org/wiki/Maximum_segment_size) <br/>
    >MSS = MTU - IP Headers - TCP Headers = 1500 - 20 - 20 = 1460
- [PMTUD - Path MTU Discovery](https://en.wikipedia.org/wiki/Path_MTU_Discovery) <br/>
    is a standardized technique in computer networking for determining the maximum transmission unit (MTU) size on the  network path between two Internet Protocol (IP) hosts, usually with the goal of avoiding IP fragmentation
- [Nagle's Algorithm](https://en.wikipedia.org/wiki/Nagle%27s_algorithm) <br/>
    is a means of improving the efficiency of TCP/IP networks by reducing the number of packets that need to be sent over the network
    - CURL disables this back in 2016 by default beacause TLS handshake was slowed down
- [Delayed Acknowledgment](https://en.wikipedia.org/wiki/TCP_delayed_acknowledgment)
- [HOL blocking](https://en.wikipedia.org/wiki/Head-of-line_blocking#:~:text=Head%2Dof%2Dline%20blocking%20(,multiple%20requests%20in%20HTTP%20pipelining.) - Head-of-line blocking

```
DUP ACK - Duplicate Acknowledgements
RTT - Round-Trip Time 
Congestion Avoidance - TCP congestion control
   TailDrop
   RED/WRED
   Cubic
   BBR
FEC - Forward Error Correction
UDP Amplification Attack (DNS)
```

# [Network Types](https://en.wikipedia.org/wiki/Computer_network)

![scope.svg](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Data_Networks_classification_by_spatial_scope.svg/768px-Data_Networks_classification_by_spatial_scope.svg.png)
- PAN - Personal Area Network
- LAN - Local Area Network
- MAN - Metropolitan Area Network
- WAN - Wide Area Network

### Network Architecture


