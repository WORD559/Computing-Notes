# TCP/IP #

How does a consignment of goods reach its destination?

What processes must it undergo before being shipped?

 - Items are split into packages and numbered
 - They are boxed
 - They are labelled
 - They are put into a delivery van
 - They are sent
 
The exact reverse occurs when they are received.

 - They are received
 - They are unloaded from the van
 - The labels are checked
 - They are unboxed
 - They are combined again


This is a good analogy for the TCP/IP stack.

The TCP/IP protocol stack is a set of rules used in turn to format a message so that it can be sent over a network. Each layer provides a specific function within the transmission of the message. What happens on one side gets reversed on the other.

TCP/IP uses four connected layers to allow network communication to take place. Each layer wraps the packets with its own header data:

 - Application layer (layer 4)
 - Transport layer
 - Network layer
 - Link layer (layer 1)

## Application Layer ##

Used to provide services for applications that want to communicate across a network, often the Internet.

 - Uses high level protocols that set an agreed standard between the communication endpoints.
 - For example, SMTP (for email), FTP (for file transfer), HTTP (for web browsing)
 - Does not actually determine how the data is transmitted, rather specifies the rules of what should be sent.

A web page is requested by a client computer. As part of the web page, the following .png web image is to be requested from a web server by the client browser using the http protocol.

## Transport Layer ##

Uses the Transmission Control Protocol (TCP) to establish an end-to-end connection with the recipient computer.

 - Splits data into packets and numbers them sequentially
 - Adds the port number to be used based on the protocol
 - At the receiving end this layer confirms that packets hae been received and requests any missing packets be re-sent.

## Network Layer ##

Uses the Internet Protocol (IP) to address packets with the source and destination IP. 

A router forwards each packet towards an endpoint called a socket, defined by the combination of OP address and port number, eg: 42.205.110.140:80

Each router uses a routing table to instruct the next hop.

## Link Layer ##


The link layer operates across a physical connection. It adds the MAC address of the physical NIC that packets should be sent to based on the destination IP address. The MAC address changes every hop.


## Receiving Data ##

At the destination, the message is passed back up through the layers.

 - The Link Layer removes the MAC address from each packet and passes it to the network layer.
 - The Network Layer checks the IP address and then removes it from each packet if this is the destination, and passes it to the transport layer.
 - The Transport Layer removes the port number from each packet, reassembles the packets in the correct order, and passes them to the application layer.
 - The application layer handles the received data.


## MAC Addresses ##

A MAC address uniquely identifies a physical device with a Network Interface Card.

This may be the destination computer, or a router in transit. Packets move up and down the lower layers of the stack as the hop across routers, changing their source and destination MAC address as they go.

As a packet leaves your computer, the destination MAC address would be the first hop, probably your router.


## Port Numbers ##

A port is used to alert a specific application to deal with data sent to a computer. These are used by protocols to specific what data is being sent.
The compination of an IP address and a port number, separated by a colon, is known as a socket.

### FTP ###

File Transfer Protocol is an application level protocol used to move files across a network.

 - FTP uses the client server model with separate data and control channels operating on ports 20 and 21.
 - Usernames and passwords are frequently used to protect access to files and to identify users.
 - Access can also be provided anonymously where any user can access the FTP site.

### Secure Shell ###

Secure Shell (SSH) is an encrypted protocol that allows secure communication between nodes across a network.

SSH uses public key encryption to protect the data in communication and is commonly used for remote management of servers and other computers.

SSH can be used to create a tunnel through a network. For example, if a port is blocked by a firewall but SSH is not (though you can use any port), you can use SSH to tunnel to another computer which does not block this port and access data that might otherwise be blocked.

### Sending and Receiving Emails ###

Mail servers are dedicated computers responsible for storing emails, providing access to clients and providing services to send emails.

They use three protocols:

 - SMTP: Used to send emails and forward them between mail servers to their destination.
 - POP3: Downloads email stored on a remote server to a local client (usually removed after download, but you can instruct the POP3 server not to delete it for a short while)
 - IMAP: Manages emails on a server so multiple clients can access the same email account in synchronicity. Data remains on the server.

### Web Servers ###

Dedicated computers that host websites and provide resources on request.

HTML, CSS, and JavaScript are separated and broken down into their constituent parts e.g. `<HEAD>` and `<BODY>`

These text elements are further broken down and rendered on the client browser according to a standard hierarchical model, though some web browsers don't conform to the standard.

Other page resources such as images, videos or scripts are subsequently downloaded as the page is rendered.


# IP Addresses #

What is an IP address? An IP address is a unique numerial identifier for a host computer or network node tryin to communicate over IP on a network.

The IPv4 standard uses four octets when written in a decimal-dotted notation. This produces a range of addresses from 0.0.0.0 - 255.255.255.255. 

Some IP addresses are reserved for other purposes, such as 10.x.y.z, 172.16.0.1 to 172.31.255.255, and 192.168.y.z are private, non-routeable addresses used for LANs or private WANs. x.y.z.0 represents an entire network. The last address in a network (x.y.z.255) is resserved as the broadcast address on that network for sending data simultaneously to all hosts on a network. 127.x.y.z is reserved for loopback, in which a host's IP software treats an outgoing packet as input.

IPv4 only provides a theoretical maximum of 2^32 or 256^4 = 4.3 billion addresses, which is not enough for the number of devices that need them.

IPv6 uses 128 bits expressed as a string of 32 hexadecimal digits, for example: 3dfb:1730:4935:0007:0340:fe2f:fb71:48af


An IP address consists of two parts:

 - Network identifier (or network ID): left-hand bits of 32-bit number, used to define the network where nodes are communicating
 - Host identifier (or host ID): right-hand bits of 32-bit number, used to identify separate nodes on the network

Since the two IDs occupy complementary sets of bits within the IP address, they can be added together to form the IP address.

|IP Address    | Network ID | Host ID|
|:------------:|:----------:|:------:|
|142.67.57.253 | 142.67.0.0 | 57.253 |
|142.67.128.86 | 142.67.0.0 | 128.86 |

It can, however, be split at other points.

The more hosts you have in a network, the fewer networks can be created. For example:

 - The network 210.54.101.0/24 has a network ID of 24 bits, as confirmed by the classless suffix /24
 - This leaves 8 bits for the host ID, which provides 254 useable host IDs. However, there are 2^24 similar network IDs available to create
 - The network 125.0.0.0/8 provides 2^24 -2 host IDs, but only 256 different networks could exist.

Too many hosts as a flat space can make the network unmanageable.


IP addresses used to be categorised into classes to identify the network and host IDs of various ranges. Now we use classless IP addressing.

After the IP address, the use of a suffix such as /24 enables IP addresses to be used with varying proportions of network and host ID.

 - IP addresses are now used without classes
 - The subnet mask is used to define the Network ID and this can be segmented however a network administrator sees fit

A subnet mask is used together with an IP address to identify the network identifier within the address. The subnet mask has all network ID bits set to 1 and all host ID bits set to 0 so that, when compared to the IP address using a bitwise AND operation, the network is identified. 