# Client-Server Model #

A host or client computer on a network contacts a server to request something.

- File server/FTP sever - files
- Email server - emails
- Proxy server - copies of web pages
- DHCP server - IP address, subnet masks, etc.
- Print server - print status
- Database server - records

Network services are designed to act as on-demand services where the server is responsible for the bulk of the processing.

 - A server presents its services to requesting clients
 - If the request cannot be fulfilled a suitable notification will be sent


## Application Programming Interface ##

Servers often provide a programmable interface to their services.

- An API is a set of functions and protocols that clients can use
- A server-side web API is a set of web services or web resources to enable programmers to build web applications
- Sometimes, programmers use multiple server-side web APIs to created combined web applications called mashups.
    - For example, programmers might use the APIs of Spotify and Google Maps to build a mashup website that combines a music playing application with an interactive map.

An API can be initialised in a web page as easily as this: 
`<script src="https://maps.googleapis.com/maps/api/js"></script>`

The process is initialised and defined by the client. Once the API has been initialised, the web page can define how to interact and request data.

The advantage of using an API is that you can use services that are not your own in creating another useful service.

## HTTP Connections ##

Limitations:

 - Client has to "pull" data from the server
 - If too much time passes between establishing a socket connection between client and server and receipt of a request, the server drops the connection to conserve its resources and returns an error message.

To combat this, we use the WebSocket protocol that includes an API for establishing a persistent TCP socket connection.

 - Designed for web browser and server, but can be any type of client and server can use it
 - Connection is full-duplex (simultaneous two-way)
 - Allows client and server to send data at any time
 - Server can offer "push" data to the client
 - WebSocket Secure is encrypted

Any dynamic/responsive applications, where response times are important, need this type of connection. This is made more economical by establishing a trusted, open connection which reduces server load because packets can be stripped of many of the usual headers. This creates a superfast, interactive connection commonly used with websites requiring real-time updates. Server load is reduced, saving bandwidth and running costs as well as reducing the number of webservers required.

## Web CRUD Applications ##

These are four basic data manipulation operations (often referred to as CRUD)

 - Create -- Write record to database
 - Retrieve -- Retrieve record from a database
 - Update -- Amend a record
 - Delete -- Remove a record from a database

These are, in HTTP:

 - POST
 - GET
 - PUT
 - DELETE

## REpresentational State Transfer (REST) ##

REST is an architectural style which determines how systems communicate with each other.

Typically, REST uses HTTP request methods to interact with online databases. RESTful systems and APIs separate the client from the server database allowing either to be updated independently without impacting on the other.

`Browser --HTTP Request--> Web Server --Client-side JavaScript passes HTTP request to server--> Database Server`

`Database Server --JSON or XML response--> Web Server --Browser interprets JSON or XML--> Browser`

## JSON and XML ##

There are two widely used formats for the standardised data objects that server and client can both process.

 - JSON - JavaScript Object Notation is written in a standard programming form, similar to JavaScript, and can be directly used by JavaScript.
 - XML - Extensible Markup Language has a format similar to HTML and wraps content in tags.

JSON:

```
{"dinosaurs":[
{"name":"Brachiosaurus","lengthM":30,"period":"Jurassic"}
]}
```

XML:

`insert example here`

JSON Advantages:

 - Can be used natively in JavaScript
 - Easier for a human to read , write, and maintain
 - More compact, so requires less storage and quicker to transmit
 
Disadvantages:

 - Works with a limited range of datatypes

XML Advantages:

 - Any data type allowed so much more flexible
 
Disadvantages:

 - Expansive use of tags makes it more difficult to follow


## Thick Clients ##

The easiest way of implementing a network is to use standard computers as hosts and join them via a network medium.

 - Each host on the network would be a powerful computer in its own right.
 - Unfortunately this power is relatively expensive and each node needs to be administered indivudually.
 - Each host needs the resources to be able to run the software on the computer.

## Thin Clients ##

An alternative is to use low-powered processors in hosts specifically designed as network machines.

 - The processing is done on a powerful central server and the hosts are only required to display the results and provide user input
 - Thin client has a simple operating system requiring little maintenance or administration
 - A 'zero' client can download the latest OS version and its configuration from a server each time a user turns it on
 - Whilst there is a cost saving from not requiring multiple powerful individual machines, a powerful server and a highly responsive network infrastructure are required

## Thick vs Thin ##

 - Thin clients are considerably more secure than thick, because the copy of an operating system can be non-persistent -- any changes to the OS can be reverted simply by rebooting
 - Thin clients require much more network bandwidth
 - Thin clients require a beefier server or server farm
 - Thin clients don't really need to be security hardened, only really the server
 - Thin clients do not really support powerful applications because of the server requirements
 - Many pieces of software do not support the shared model of thin clients
 - Thin clients are much easier to update
 - Thick clients are able to operate without a connection to the server
 - Thick clients are generally more reliable