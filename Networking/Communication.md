# Communication #

- Series or parallel
- Bandwidth, bitrate, baud rate
- Latency
- Synchronous/asynchronous
- Handshaking
- Protocols and their transmissions

## Serial vs Parallel Transmissions ##

- Serial Transmission sends and receives data one bit at a time, eg. In a keyboard.
- Serial connections are used to connect most of the peripherals.
- Serial cables can be used to connect computers together to form a network.
- Parallel data transmission uses a number of wires to send a number of bits simultaneously. The more wires there are, the moredata can be sent at any one time.
- Parallel transmission is used by buses. A 32-bit parallel connection, for example, may connect the processor and memory together.
- Serial is not slow! They are still quite quick. Compared to parallel, however, they are typically slower.

## Bandwidth ##

- Bandwidth is the term used to describe the amount of data that can be transmitted along a communication channel.
- It relates to the range of frequenciesthat are available on the carrier wave that carries the data.
- The range in this case is the difference between the upper and lower frequencies.
- As the range of frequencies increases, the amount of data that can be transmitted within the same timeframe also increases.
- Bandwidth is measured in Hz and MHz.

## Bitrate ##

- Bitrate is the speed at which a particular transmission is taking place, the number of bits that can be transmitted in a period of time.
- It is closely linked with bandwidth, as the bitrate is directly proportional to how much bandwidth is available.
- Bitrate is measured in bits per second.

## Baud Rate ##

- The baud rate is the rate of electronic state change in a device.
- 1 Baud means 1 change per second.
- Traditionally, one bit is sent on each state change, so one baud is normally about one bit per second.
- It is possible to send more than one bit per state change, though, using different voltages to represent the different bits.

## Latency ##

- The general term for the time delay between an action happening and its results being seen.
- This is because the instruction is being transmitted down cables, and through buses and logic gates, which all takes time.
- Latency can occur at any stage in the transmission process.
- These delays could be so short they are unnoticeable.
- It can be dependant on the transmission medium and the network traffic.
- Pinging is a good way to measure latency.

### Types of Latency ###

- Propagation Latency -the amount of time is takes for a logic gate within a circuit to transmit the data.
- Transmission Latency -the amount of time it takes to pass through a particular communication medium, for example, fibre optic would have a lower latency than copper cable.
- Processing Latency -the amount of time it takes data to pass around a network depending on how many servers or devices it has to pass through.

## Synchronous Data Transmission ##

- The two devices will synchronise their transmission signals in synchronous transmission.
- Using the system clock, the transmitting computer will control the transmission rate to be in time with the computer receiving the data.
- If they are unsynchronised, data could be lost in the transmission.

## Asynchronous Data Transmission ##

- Asynchronous data transmission does not require permanent synchronisation of the system clocks, instead synchronising only for the duration of the transmission.
- It does this by sending additional bits of information, start and stop bits.

## Handshaking ##

- There are so many manufacturers of hardware and so many ways of transmitting data that it is essential that there are accepted standards for data transmission.
- Handshaking establishes a connection between two devices and establishes the rules under which they will communicate.

## Protocols ##

- A protocol is a set of rules established in handshaking.
- TCP/IP (Transmission Control Protocol/Internet Protocol) is actually two protocols that are usually referred to as one and relate to the set of rules that govern the transmission of data around the Internet
- HTTP (hypertext transfer protocol) is the set of rules governing the exchange of the different file types that make up displayable web pages.
- FTP (File Transfer Protocol) is similar to HTTP in that it provides the rules for the transfer of files on the Internet.