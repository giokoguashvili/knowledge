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
SSL VPN                 - Secure Sockets Layer Virtual Private Network
IPsec                   - IP Security
GRE                     - Generic Routing Encapsulation

PAT                     - Port Address Translation
NAT                     - Network Address Translation

SSH                     - Secure Shell
Telnet                  - an application protocol used on the WAN or LAN to provide a bidirectional interactive text-oriented communication facility using a virtual terminal connection

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
    NDP (IPv6)          - Neighbor Discovery Protocol

Network Layer   
    IP (IPv4/v6)        - Internet Protocol version 4/6
    DHCP                - Dynamic Host Configuration Protocol
    STP                 - Spanning Tree Protocol 
    RIP                 - Routing Information Protocol
    OSPF                - Open Shortest Path First
    BGP                 - Border Gateway Protocol
    ICMP                - Internet Control Message Protocol
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
```
