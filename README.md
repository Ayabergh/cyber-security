# cyber-security
Dynamic Host Configuration Protocol

The Dynamic Host Configuration Protocol (DHCP) is a network management protocol used on Internet Protocol (IP) networks for automatically assigning IP addresses and other communication parameters to devices connected to the network using a client–server architecture.
DHCP can be implemented on networks ranging in size from residential networks to large campus networks and regional ISP networks. Many routers and residential gateways have DHCP server capability. Most residential network routers receive a unique IP address within the ISP network. Within a local network, a DHCP server assigns a local IP address to each device.
DHCP services exist for networks running Internet Protocol version 4 (IPv4), as well as version 6 (IPv6). The IPv6 version of the DHCP protocol is commonly called DHCPv6.
Internet Protocol (IP) defines how devices communicate within and across local networks on the Internet. A DHCP server can manage IP settings for devices on its local network, e.g., by assigning IP addresses to those devices automatically and dynamically.
On large networks that consist of multiple links, a single DHCP server may service the entire network when aided by DHCP relay agents located on the interconnecting routers. Such agents relay messages between DHCP clients and DHCP servers located on different subnets.
Depending on implementation, the DHCP server may have three methods of allocating IP addresses:
Dynamic allocation
A network administrator reserves a range of IP addresses for DHCP, and each DHCP client on the LAN is configured to request an IP address from the DHCP server during network initialization. The request-and-grant process uses a lease concept with a controllable time period, allowing the DHCP server to reclaim and then reallocate IP addresses that are not renewed.
Automatic allocation
The DHCP server permanently assigns an IP address to a requesting client from a range defined by an administrator. This is like dynamic allocation, but the DHCP server keeps a table of past IP address assignments, so that it can preferentially assign to a client the same IP address that the client previously had.
Manual allocation
This method is also variously called static DHCP allocation, fixed address allocation, reservation, and MAC/IP address binding. An administrator maps a unique identifier (a client id or MAC address) for each client to an IP address, which is offered to the requesting client. DHCP servers may be configured to fall back to other methods if this fails.
DHCP services are used for Internet Protocol version 4 (IPv4) and IPv6. The details of the protocol for IPv4 and IPv6 differ sufficiently that they may be considered separate protocols.[8] For the IPv6 operation, devices may alternatively use stateless address autoconfiguration. IPv6 hosts may also use link-local addressing to achieve operations restricted to the local network link.


Domain Name System

The Domain Name System (DNS) is the hierarchical and distributed naming system used to identify computers reachable through the Internet or other Internet Protocol (IP) networks. The resource records contained in the DNS associate domain names with other forms of information. These are most commonly used to map human-friendly domain names to the numerical IP addresses computers need to locate services and devices using the underlying network protocols, but have been extended over time to perform many other functions. The Domain Name System has been an essential component of the functionality of the Internet since 1985.
An often-used analogy to explain the DNS is that it serves as the phone book for the Internet by translating human-friendly computer hostnames into IP addresses. For example, the hostname www.example.com within the domain name example.com translates to the addresses 93.184.216.34 (IPv4) and 2606:2800:220:1:248:1893:25c8:1946 (IPv6). The DNS can be quickly and transparently updated, allowing a service's location on the network to change without affecting the end users, who continue to use the same hostname. Users take advantage of this when they use meaningful Uniform Resource Locators (URLs) and e-mail addresses without having to know how the computer actually locates the services.
An important and ubiquitous function of the DNS is its central role in distributed Internet services such as cloud services and content delivery networks. When a user accesses a distributed Internet service using a URL, the domain name of the URL is translated to the IP address of a server that is proximal to the user. The key functionality of the DNS exploited here is that different users can simultaneously receive different translations for the same domain name, a key point of divergence from a traditional phone-book view of the DNS. This process of using the DNS to assign proximal servers to users is key to providing faster and more reliable responses on the Internet and is widely used by most major Internet services.
The DNS reflects the structure of administrative responsibility on the Internet.Each subdomain is a zone of administrative autonomy delegated to a manager. For zones operated by a registry, administrative information is often complemented by the registry's RDAP and WHOIS services. That data can be used to gain insight on, and track responsibility for, a given host on the Internet.


Address Resolution Protocol

The Address Resolution Protocol (ARP) is a communication protocol used for discovering the link layer address, such as a MAC address, associated with a given internet layer address, typically an IPv4 address. This mapping is a critical function in the Internet protocol suite. ARP was defined in 1982 by RFC 826, which is Internet Standard STD 37.
ARP has been implemented with many combinations of network and data link layer technologies, such as IPv4, Chaosnet, DECnet and Xerox PARC Universal Packet (PUP) using IEEE 802 standards, FDDI, X.25, Frame Relay and Asynchronous Transfer Mode (ATM).
In Internet Protocol Version 6 (IPv6) networks, the functionality of ARP is provided by the Neighbor Discovery Protocol (NDP).
The Address Resolution Protocol is a request-response protocol. Its messages are directly encapsulated by a link layer protocol. It is communicated within the boundaries of a single network, never routed across internetworking nodes.
ARP's placement within the Internet protocol suite and the OSI model may be a matter of confusion or even of dispute. RFC 1122 mentions ARP within its link layer section without explicitly placing it within that layer. Some older references place ARP in OSI's data link layer while newer editions associate it with the network layer or introduce an intermediate OSI layer 2.5.
An ARP probe in IPv4 is an ARP request constructed with the SHA of the probing host, an SPA of all 0s, a THA of all 0s, and a TPA set to the IPv4 address being probed for. If some host on the network regards the IPv4 address (in the TPA) as its own, it will reply to the probe (via the SHA of the probing host) thus informing the probing host of the address conflict. If instead there is no host which regards the IPv4 address as its own, then there will be no reply. When several such probes have been sent, with slight delays, and none receive replies, it can reasonably be expected that no conflict exists. As the original probe packet contains neither a valid SHA/SPA nor a valid THA/TPA pair, there is no risk of any host using the packet to update its cache with problematic data. Before beginning to use an IPv4 address (whether received from manual configuration, DHCP, or some other means), a host implementing this specification must test to see if the address is already in use, by broadcasting ARP probe packets.
ARP mediation refers to the process of resolving Layer-2 addresses through a virtual private wire service (VPWS) when different resolution protocols are used on the connected circuits, e.g., Ethernet on one end and Frame Relay on the other. In IPv4, each provider edge (PE) device discovers the IP address of the locally attached customer edge (CE) device and distributes that IP address to the corresponding remote PE device. Then each PE device responds to local ARP requests using the IP address of the remote CE device and the hardware address of the local PE device. In IPv6, each PE device discovers the IP address of both local and remote CE devices and then intercepts local Neighbor Discovery (ND) and Inverse Neighbor Discovery (IND) packets and forwards them to the remote PE device.


