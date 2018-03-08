# Packet Switching and Routers #

Circuit switching involves creating a communication connection between two endpoints for the duration of a phone call or transfer of data. However this does not work for the billions of inter-connected parts of the Internet.

Packet switching was developed to allow a communications channel to be shared so that when one communication was temporarily not using it another could.

When sending across a network, data is broken into units called data packets and these are assembled again at the receiving end. This increases network efficiency and reliability. One reason for this is because if any data was dropped during the connection, the receiving computer can re-request just the damaged packets instead of requiring the entire file again.

## Chunking Data ##

Consider a 10GB video file.

If each packet contains 1,500 bytes of data:

 - 10,000,000,000 bytes to send
 - 10,000,000,000/1,500 = 6,666,667 packets

## Packet Switching ##

Packets are often sent across networks that have multiple links with multiple routes through to a destination. These networks are also often shared.

Each packet takes the fastest available route.

Assume a packet is travelling from London to Sydney, Australia. This might take 40ms to reach its destination. In comparison, a packet from London to Paris might only take 5ms. This is known as latency.

## Routing ##

Routers forward data packets from one network to another. Each router stores data about the available routes to the destination node. It looks up the destination IP address in its routing table to find the best router to which to forward the packet. Each forwarding by (or transfer across) a router is known as a hop. Routers continue to forward the packet until it reaches its destination node.

The router does not actually know where the end node is, it just knows the adjacent nodes. Complex routing algorithms then redirect the packets around the world without any real idea where they're going.

## Building a Packet ##

At its core, a data packet is a segment of data that needs to be sent, referred to as a payload.

This part of the packet will vary in size, from 500 to 1500 bytes.
Packets also include additional information called headers and trailers.

`--[Trailer. End of packet, checksum][Payload. Data][Header. Sender IP, Recipient IP, Protocol, Packet number x and y]-->`

Packets have to be quite small, because nothing else can use the same connection as you while you're using transferring it. It is not a direct physical connection, and other people will want to use the connection while you are using it. By breaking up the data into small packets, they do not take an excessive amount of time to transfer, preventing other packets from moving. If they are too small, however, then the amount of data actually sent in the payload would be too small due to the headers and trailers, as they are essential to the transfer. 500-1500 bytes is an ideal compromise.

### Packet Header ###

The header contains the recipient's address address so that it can be directed appropriately across the network. 
The sender's address is also included so that replies can be sent appropriately.
The packet number and overall number of packets in the transmission is attached to assist in reassembling the data.
The Time To Live (TTL) or hop limit is also included to kill off the packet after a certain amount of time and prevent it from going around the world endlessly.

### Packet Trailer ###

Similarly, at the end of the packet a trailer is added.

This contains error checking components that verify the data received in the payload has not been corrupted on transfer. Techniques such as checksums or Cyclical Redundancy Checks (CRCs) are used to check the data by the receiving host. The same checksum is recalculated at the destination end. If they do not match, the data has become corrupted and is refused, and a new copy is requested to be sent again.

## Gateways ##

A gateway is required where data is travelling from one network to another that use different protocols.

Networks using different transmission media can require this. Header data are removed and reapplied using the correct format of the new network. A router and a gateway can often be combined into one integrated device. These are still two different parts, the gateway just translates the packets for a different network.