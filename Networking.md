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

Steps of the DHCP Handshake
1. Client Discovery: The client broadcasts a request for a configuration
2. DHCP Offer: Any DHCP server can respond with a configuration offer.
3. Client Request: The client broadcasts which configuration it has chosen.
4. DHCP Acknowledgement: The chosen server confirms that its configuration has been given to the client.

Wi-Fi: A layer 2 protocol that wirelessly connects machines in a LAN.
1. Access Point: A machine that will help you connect to the network.
2. SSID (Service set identifier): The name of the Wi-Fi network.
3. Password: Optionally, a password to secure Wi-Fi communications.

Wi-Fi Protected Access 2 (WPA2): A protocol for securing Wi-Fi network communications with cryptography. Design goals:
1. Everyone with the Wi-Fi password can join the network.
2. Messages sent over the network are encrypted with keys
3. An attacker who does not know the Wi-Fi network cannot learn the keys.

WPA Handshake

WPA-Enterprise: Core issue is that every client has the same PSK to derive the PTK. The fix is to have each user use their own username and password.
1. Instead of using a PSK, use a randomly generated key by an authentication server
2. For your client to trust the authentication server, you accept a digital certificate
3. Form a secure channel to the authentication server, which lets you enter your username and password
4. If the username and password are correct, the authentication server sends a one-time key to use instead of a PSK to both the client and the AP (also over a secure channel) 

Routing packets:
To send a packet to a computer within the local network:
- Verify that the destination IP is in the same subnet
- Use ARP (or contact a switch) to get the destination MAC address
- Send the packet directly to the destination using the destination MAC address
To send a packet to computer that is not within the local network:
- Send the packet to the gateway
- Past the gateway, the packet goes to the Internet
- It’s the gateway’s job to deliver the packet closer to the destination



# Readings
[Network Security Portion of CS161](https://textbook.cs161.org/network/)
