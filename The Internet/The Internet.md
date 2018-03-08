# Internet #

You are accessing a website in New York from a computer in London.

How does the request get there and back?


The Internet is the largest public network in the world.

The Internet is a network of inter-connected networks, hence inter-net. 

The World Wide Web os a collection of resources accessed via the Internet.



## Directing Traffic ##

Similar to a road network, data traffic is directed to any location if the destination address is known.

The main part of the Internet is known as the backbone. This is a set of dedicated connections that connect several large networks at various points on the globe. Each of these points are then connected to other regional networks usually, controlled by Internet Service Providers. An ISP provides access to individual end-users.

What happens when data are sent from Belgium to New York? 

What happens to the same data if all backbone connections from Europe to the USA are disconnected?

What happens if one conection across the channel is damaged?

In these cases the traffic can be rerouted around the world to maintain the connection, albeit slow.

What happens if both backbone connections to the far north of Scotland are damaged?

If there are no other connections to the islands, the traffic cannot be rerouted. They are disconnected.

## Internet Addresses ##

Each device on a network needs to be uniquely identified so that data can be sent to the correct destination, much like an address on a letter. The Internet Protocol (IP) addressing system is used.

IPv4 addresses are made up of four octet values separated by a full-stop. Eg. `14.132.250.10`

This provides only 4.3 billion addresses for 7 billion people.

IPv4 is no longer enough, so IPv6 is used to extend this enough for 340,282,366,920,938,463,463,374,607,431,768,211,456 different addresses.

The most common method of addressing is that your router is given a single public IP address, and all the devices on your network are privately addressed in the `192.168.xxx.xxx` range. All traffic is sent to the router's public IP, and the router directs the traffic to the correct device.

IPv6, however, has enough addresses available for every device to have its own static public IP address.


An FQDN is a Fully Qualified Domain Name. For example, 

- bbc.co.uk is the domain name
- www. specifies the host
- www.bbc.co.uk is the the FQDN

A URL (Uniform Resource Locator) is a means of accessing a resource and its location across a network.

The protocol and the domain name of the resource together form a URL. For example,
   
- http:// specifies that the resource requires http (a web page)
- www.bbc.co.uk is the FQDN
- index.html is the resource to be accessed
- http://www.bbc.co.uk/index.html is the full URL

## DNS ##

Domain Name System.

DNS Servers are dedicated computers with an index of domain names and their corresponding IP addresses. When a computer queries a DNS server for a domain name, the server returns an IP address that the computer can use to connect to it.

Using domain names over IP addresses makes the addresses more human-readable and memorable.

There are several DNS servers that work together to catalogue every web domain name. These are segmented into geographical groupings or levels.
When the IP address of a given domain is not known, a query is referred to a related domain server that could know.

```

                          Root
           +----+----+-----+---+---+
         .com .edu .org   .uk .fr .de
                           |
                      +----+----+
                     .co .gov .sch
                      |
                 +----+----+
                bbc ebay lidl
```

DNS is often cached by your computer, your router, or other local DNS servers to speed up access.

### Resolving an IP Address ###

1. check local DNS Server
2. not in local DNS -- refer to root
3. root may know, or may just know where the server for the next layer is
4. this continues until the IP address is found
5. the IP is then returned to the client

This process goes from right to left, e.g. root -> .uk -> .co -> bbc


If the DNS service is disrupted, then it can produce a lack of internet connection. The medium for the Internet is still fully operational, but your computer will be unable to resolve IP addreses. This can be averted by locally caching DNS queries. For example, you may go to google.com and receive an IP address from the DNS server. Your router caches this, and then if the DNS server stops working, your router is able to provide the IP address for Google instead of the DNS server.

There are five global internet registries that are responsible for allocating addresses to specific domain names. These registries work together to maintain a database of address assignments that ensure that IP addresses and domain names are unique.

They must be unqiue because otherwise a single domain name could point to multiple IP addresses.

bbc.com and bbc.co.uk are both allowed, because they are different top level domains.


While domain names should point to unique IP addresses, that may not always be the same IP address. If you do a DNS lookup for Google one day, the IP will likely be different the next day.

## Purchasing a Domain Name ##

Available domain names are issued by Internet registrars, e.g. www.1and1.co.uk



# Internet Security #

 - Understand how a firewall works
 - Explain symmetric and assymetric encryption and key exchange
 - Explain how digital signatures and certificates are obtained and used
 - Discuss worms, trojans and viruses and the vulnerabilities they exploit
 - Discuss how improved code quality, monitoring and protection can be used against such threats


A file is being transferred from Chile to India.
What risks are involved in sending confidential information within the file?


How do you get in or out of a castle?

 - What can you do to stop people entering of leaving?

## Firewall ##

The entrance to a network can be protected in the same way by a firewall.

 - A firewall is either software or hardware that controls access to and from a network.
 - Numbered doors called 'ports' are opeed so that only certain traffic is allowed to pass through.

### Stateless Inspection Packet Filtering ###

Packets of data are inspected by the firewall to check which port they are attempting to access. Different network protocols use different port numbers. For example, HTTP traffic is on port 80 or 8080.

If this traffic is to be allowed through, the port must be opened for the duration of the connection, otherwise the firewall will automatically reject it.

All the ports are closed by default unless allowed. Otherwise it's much like leaving your front door open.

This is a very crude method.

### Stateful Inspection ###

Rather than relying on port numbers and IP addresses to determine passage, stateful inspection examines the payload of a packet before allowing access and remembers actions for future decisions.

When data are expected from a destination they are allowed through as the details of the 'conversation' are maintained by the firewall.

## Proxy Server ##

A proxy server makes a web request on behalf of your own computer, hiding the true request IP addresses from the recipient.

Web page is gotten from either the remote server or from the proxy's cache. Any requests appear to go from the proxy, not you.

Proxies:

 - Enable anonymous surfing
 - Can be used to filter out undesirable content
 - Logs user data with their requests
 - Provides a cache of previously visited sites to speed access

## Encryption ##

The act of encoding a plaintext message so that it cannot be deciphered unless you have a numerical key to decrypt it.

### Symmetric Encryption ###

Symmetric encryption uses the same key to encrypt as to decrypt. The key has to be transferred between the communicating devices so that they both know how to encrypt and decrypt the messages.

However, if this key is acquired by a malicious user, a man-in-the-middle attack can be performed to intercept and read the data pretending to be the other party. The encryption is rendered useless.

Advantages:

 - Relatively fast

Disadvantages:

 - Communicating devices have to transfer the key between them so that they both understand how to communicate. If it is intercepted, an attacker can also decrypt the messages.

### Asymmetric Encryption ###

Asymmetric encryption uses two separate but related keys. One is able to encrypt the data (the public key) and one is able to decrypt the data (the private key). This has certain limitations (i.e. data size) but can be used to negotiate keys for symmetric encryption. 

Many algorithms also work both ways (i.e. you can encrypt data with the private key and decrypt with the public key in order to, for example, encrypt a checksum for validating data.)

This is used to initiate SSL connections.

Advantages:

 - Very secure, because only one person needs to know how to decrypt it

Disadvantages:

 - Considerably slower than symmetric encryption
 - Need to validate that the key you're using belongs to your intended recipient!