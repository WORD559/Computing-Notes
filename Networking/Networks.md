# Networks #

- Components that are needed to construct a network, including servers, clients, routers, switches, and network cards
- How networks can be constructed using different topologies
- The benefits of different topologies
- How networks can be client-server or peer-to-peer
- How wireless networks work
- How data is transmitted in frames and packets
- How data being transmitted used protocols to prevent collisions of data and keep data secure

## Basics ##

- In order to connect to a network, a computer must have a network adapter, more commonly known as a Network Interface Card, NIC.
- The NIC is a printed circuit board contained within the computer like any other card (eg. Sound Card or Graphics Card)
- The NIC is specifically designed to allow the computer to connect, either by cable or by wireless, to a specific network topology
- The type of card also dictates the speed of data transmissions that will be available between this device and the network

## Local and Wide Area Networks ##

- Networks are described in terms of the geographical area that they cover, and the way in which they are configured (the network topology)
- A Local Area Network (LAN) is a number of computers and peripherals connected over a small geographic distance, covering one building or site.
- A Wide Area Network (WAN) is a number of computers and peripherals connected together over a large geographical distance, normally across different sites.
- If it isn't a LAN, it's a WAN. That simple.
- The moment it goes beyond a single site, it becomes a WAN.

## The Router ##

- Receives every packet of data being transmitted, reads the header of the packet and then forwards it to it's destination.
- Can act as a firewall, preventing certain packets from being forwarded.
- Can act as a switch, creating a connection between two devices on a network.
- Can provide a wireless access point transmitting a Wi-Fi signal.
- Can act as a modem to convert digital signals to analogue so that they can be transmitted down standard telephone cables.

## Topologies ##

Topologies describe the logical layout of a network -they don't always look physically like the description.

### Star Topology ###

- Each client has a dedicated connection to the server.
- If one connection is broken, the other clients can still access the server.
- In reality, the server is connected to a switch, and the clients connect to the switch instead.
- The server will be a high specification machine with a large amount of processing power and storage capacity.
- The clients can connect from cable or Wi-Fi.

#### Advantages ####

- Fast connection speed, as each client has its own connection.
- It will not slow down as much when multiple users are online.
- Fault-finding is simpler, as individual faults are easier to trace.
- It is relatively secure, because every connection from client to server is unique.
- New clients can be easily added without affecting the other clients.
- If one cable or client fails, then only that client is affected.

#### Disadvantages ####

- Increased cabling costs.
- Difficult to install, as multiple cables are needed. The problem is exaggerated where the LAN splits across a number of buildings.
- The server/switch can get congested as all communications must pass through it.

### Bus Topology ###

- All nodes within the network are connected via one main cable (called the backbone).
- If there is a main server, all of the clients connect to it down this main cable.
- This cable carries data between the server and the clients, with each client branching off the main bus cable.
- The main cable (backbone) must allow high-speed data transmission, as all data must pass down this one channel.

#### Advantages ####

- It is cheaper to install than star topology as only one main cable is required.
- It is easier to install than star topology.
- It is easy to add new clients by branching them off the main cable.

#### Disadvantages ####

- It is less secure than a star network as all data is transmitted down one main cable.
- Transmission times get slower when more users are on the network.
- If the main cable fails, then all clients are affected.
- It is less reliable than a star network due to the reliance on the main cable.
- It is more difficult to find faults.

### Client-Server (this is a group of topologies) ###

- In star and bus, there is a main server.
- Although the clients have local resources in terms of processing power and storage capacity, they are controlled by the server.
- This means that when new software is installed, for example, it can be installed on the server and then distributed to the clients.
- This is the most common way of constructing a LAN with a large number of users.

### Peer-to-peer ###

- In a peer-to-peer network, no one computer is in overall control of the network.
- The resources of each computer or workstation are available to all computers in the network.
- Each workstation therefore can act either as a client or as a server, depending on the current task.
- This is more common among smaller networks or certain applications, such as file sharing.

### Wireless Networks ###

- A wireless network varies from a wired network in that it does not use cables to make physical connections between devices.
- Instead the data is sent using radio waves.
- Wireless networks can be implemented over small or large geographical distances so it is possible to have wireless LANs (WLAN) and wireless WANs (WWAN).
- All devices on a network have what is called a Media Access Control or MAC Address.
- This is a unique identifier encoded into the NIC.
- Wi-Fi is the generic term for a WLAN where devices can connect wirelessly to each other and where a connection can be made  to the internet.
- IEEE 802.11ac is marketed as Wi-Fi.
- Examples of WWANs exist. Examples include mobile phone networks and WiMAX.

#### Wireless Standards ####

- 2.4GHz is slower than 5GHz. IEEE 802.11b and g are 2.4GHz. 
    - g and b can typically go up to 100m outdoors, but around 30m indoors. 
    - 2.4GHz is more penetrating, so it may be slower but can travel through more stuff before you lose signal.
    - There is overlap in channels for 2.4GHz -1, 6 and 11 are the only channels available if you don't want interference.
- 5GHz is faster than 2.4GHz and has greater bandwidth. 
    - a is 5GHz but is an old standard, so is still slow.
    - 5GHz gives you speeds of up to 74Mbps
    - There are many more channels available to be used in 5GHz.
- Three stream wireless networks have much greater bandwidth and speed.
    - This gives you up to 400Mbps IF THE CLIENT SUPPORTS IT!!
   
## Standards ##

### Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA) ###

- This was developed to enable various devices to transmit data at high speeds without interfering with each other.
- When data is sent around networks, it is sent in frames, with all frames being re-assembled at the receiving end.
- Any device on a wireless network may attempt to send frames at any time. Before each frame is sent, the device uses the CSMA/CA protocol to see whether the transmission medium is idle of whether another device is using it.
- If the transmission medium is idle, the data is sent. If it is busy, the device will wait and try again later.
- Each device will then wait a random amount of time before checking to see if the medium is free again so it can send the data. This is known as the back-off mechanism. This means that devices who discover the medium is busy at the same won't continue to block each other -whoever gets to send first is random.

#### Request to Send/Clear to Send (RTS/CTS) ####

- The device that wants to send will send an RTS to the receiver, which will then send a CTS when the medium is idle. When it receives a CTS, it knows it is clear to begin sending data. If it does not receive one, it waits a random time before trying again.

#### Service Set Identifier (SSID) ####

- One of the issues when using wireless networks is ensuring that the various devices are connecting to the correct WLAN.
- As all of the data is being sent through radio waves rather than cables, each device needs a way of ensuring that it is connecting to the correct network.
- The standard method of doing this is using an SSID, which is a 32 character code which is put into the header of each packet of data being sent.

#### Network Security ####

- An issue with wireless technology is that it can be less secure than a wired system. To protect against threats, we can do various things.
    - Change the SSID and hide it from transmission.
    - Ensure that all devices are Wi-Fi Protected Access (WPA/WPA2) compliant.
    - Use strong encryption (WPA/WPA2) (for businesses, you can use WPA2 Enterprise)
    - Create a whitelist of MAC addresses that you know are trustworthy.
    - You can use portals to control who can access the Wi-Fi and how long they can access for, as well as get information about them should they do anything illegal.
