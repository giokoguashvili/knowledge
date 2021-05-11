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
        RJ-45
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


WAN                     - Wide Area Network
LAN                     - Local Area Network
VLAN                    - Virtual LAN
VPN                     - Virtual Private Network

IEEE - Network Protocols
    802.3   LAN   Ethernet 
    802.11  WLAN                    
RFC  - Internet Protocols
W3C  - Web Standarts

PAT                     - Port Address Translation
NAT                     - Network Address Translation

SSH                     - Secure Shell
Telnet                  - an application protocol used on the WAN or LAN to provide a bidirectional interactive text-oriented communication facility using a virtual terminal connection

Firewall        
Socket      
Gateway     

- [Internet protocol suite](https://en.wikipedia.org/wiki/Internet_protocol_suite) - wiki
- [TCP / IP protocol stack - reference map](https://informatics.buzdo.com/specific/tcp-ip-1.htm)

Data Link Layer
    ARP (IPv4)          - Address Resolution Protocol 
    NDP (IPv6)          - Neighbor Discovery Protocol

Network Layer   
    IP (IPv4/v6)	    - Internet Protocol version 4/6
    DHCP	            - Dynamic Host Configuration Protocol
    STP                 - Spanning Tree Protocol 
    RIP 	            - Routing Information Protocol
    OSPF	            - Open Shortest Path First
    BGP 	            - Border Gateway Protocol
    
Transport Layer 
    TCP	                - Transmission Control Protocol
    UDP	                - User Datagram Protocol
    RUDP	            - Reliable UDP

Session Layer   
    DNS                 - Domain Name System
    NetBIOS / IP	    - Network Basic Input/Output System over IP for TCP / IP Environment

Application Layer   
    HTTP                - Hypertext Transfer Protocol
    FTP                 - File Transfer Protocol 
    WSS                 - Web Sockets 
    SMTP	            - Simple Mail Transfer Protocol 
    TELNET	            - TCP / IP Terminal Emulation Protocol
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