# Commands
\[[Man](https://man7.org/linux/man-pages/man8/ifconfig.8.html)\]Configure/Display the current network interface configuration information:

``ifconfig``

``tcpdump``

# Tools
Wireshark: Graphical user interface for analyzing tcpdump packets

Network Switches: Connects users, applications, and equipment across a network so that they can communicate with one another and share resources. Provides additional security, isoluation, and defense against ARP spoofing. 

# Terms
- Internet: Global network of computers.
- Protocols: Agreed-upon system of communication.
- OSI (Open Systems Interconnection) model: A layered model.
- ARP (Address Translation Protocol): Translate IP address to MAC addresses.
- DHCP (Dynamic Host Configuration Protocol): Get configuration when first connecting to a network.
- WPA (Wi-Fi Protected Access): Communicate securely in a wireless local network.


# Concepts
5 main layers (High to low) in OSI that's still relevant.
1. HTTP (Application): Applications and services
2. TCP (Transport): Transportation of data
3. IP (Network): Global packet delivery
4. Ethernet (Link): Local frame delivery
5. Wires (Physical): Communication of bits

DHCP (Initial Network configuration) - to connect to a network, a user needs:
1. An IP address so that other people can contact the user.
2. The IP address of the DNS server.
3. The IP address of the router (gateway) so that the user can contact machines outside of the LAN.
The first time a user connects, they don't have this information yet. The user also doesn't know who to ask for this information. DHCP gives the user a configuration when they first join the network.

# Readings
[Network Security Portion of CS161](https://textbook.cs161.org/network/)
