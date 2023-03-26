# Computer Networking

**Computer Network** - In simple terms - Computers connected together.

**Internet** - Collection of computer networks.


## How internet started?

Cold war - United States and Soviet Union - Battle of technologies - Soviet Union created Sputnik - United States created ARPANET for communication - Advanced Research Projects Agency Network - First computer network.
(MIT - Stanford - UCLA - Utah)

- Used TCP/IP (Transmission Control Protocol) - For communication between computers.

- Previously missing automated sharing - Here WWW (World Wide Web) was introduced - Stores documents and information - Tim Berners-Lee - Published on web servers - Based on hyperlinking of web pages.

- No search engine - Couldn't search for things - Save things in indices but not search - Built search engines - Yahoo being the first.

- Protocols - Necessary for communication - Decisions made by the *Internet Society* - To make submissions use RFC (Request for Comments) - Idea/Features.


## Client-Server Architecture

- google.com - Client - Sends request to server - Server sends response - Client displays response.

- Connections over continents and countries are made under the ocean - Fiber optic cables - Light pulses - Faster than radio waves - Less interference - More bandwidth - More expensive.

- A computer can be both client and server - Example: when using localhost.

- Use `inspect element` to see Networks tab in Chrome - Shows requests and responses - Can see the time taken for each request.

## Protocols

- Set of rules - Defined by the *Internet Society*.

### TCP

- Transmission Control Protocol

- It will ensure that the data is delivered to the destination and will not be courrupted.

### UDP

- User Datagram Protocol

- Do not care whether 100% of the data is delivered or not.

- Example: Video Conferencing

### HTTP

- Hyper Text Transfer Protocol

- Used by web browsers - WWW

- Defines format of the data being transferred bw clients and servers.


## How is data transfered?

- Data is sent in chunks called **Packets**.

> NOTE: Check Chrome Dev Tools > in Network Section > see all the API requests.

- IP Address is like a phone number - Unique to each device.

### IP Address Format

> X.X.X.X
> Each X is a number between 0 and 255.

Check IP Address of your computer:
```
$ curl ifconfig.me -s
```

### How IP Addresses are assigned?

Internet Service Provider provides us with a Modem or Router - It has a global IP Address - All the devices connected to the router will have the same IP Address for everyone around the world. (Such as Printer, Mobiles, etc.)

The Modem or Router will give IP Addresses to each of the devices connected to it, called the **Local IP Address**.

How does the Modem assign the Local IP Addresses?

Using DHCP (Dynamic Host Configuration Protocol). Set 
of rules to assign IP Addresses.

> If we make a request to Google.com, google will see the global IP Address. It will not know which device is making the request. So, it will send the response to the global IP Address. 

>The Modem will then forward the response to the device that made the request using NAT(Netwrork Address Translation).

How does the NAT know which application to forward the response to?

> Let's say we're running Mongo DB, make a request, and we want the response to be forwarded to the Mongo DB application.

**IP Address** decides which device to send the data to. 

**Port** decides which application to send the data to.

> Applications differ by the port number they use.


## Ports

Ports are 16-bit numbers.

> 16 cells that contain 0 or 1 -> 2^16 = 65536 total port numbers possible.

All the requests made by the browser are made to port `80`. (All the HTTP Stuff)

HTTP = 80
MongoDB = 27017

- All ports from 0 to 1023 are reserved ports for system use.

- Ports from 1024 to 65535 are reserved for use by applications.

- Remaining ports are free and can be used.

Your Computer -> Internet Service Provider (ISP) -> Another Computer

> Tier 1 ISP - Tata (In India) (Tata has a long cable from Chennai to Singapore)

> Tier 2 ISP - Airtel (In India)

- 1 mbps -> 1 mega bits per second -> 1 million bits per second. (10^6)

- 1 gbps -> 10^9 bits per second. [Very Fast]

- 1 kbps -> 10^3 bits per second. [Very Slow]

Upload -> When you send data to the internet.

Download -> When you receive data from the internet.


## Communication between two computers

- Guided way - Set of path already defined - Example: Telephone lines.
- Unguided way - No path defined - Example: Radio waves, Bluetooth.

### How are countried connected with each other?

Go to: https://www.submarinecablemap.com

Wires across the ocean - Single wire across continents

> Google owns a lot of them.

#### Guided 

- Optical Fiber
- Coaxial

#### Wireless

- Bluetooth
- WiFi
- 3G
- 4G
- LTE
- 5G

> Cables are faster than satellites.


## Connections

### LAN (Local Area Network)

- For small house / office.
- In an area.
- Connect as many devices as you want.
- Connect via Ethernet cable, Wifi.

### MAN (Metropolitan Area Network)

- Areas of a city.

### WAN (Wide Area Network)

- Across Countries.
- Using optical fiber cables.

#### SONET (Synchronous Optical Network)
Carries data using optical fibre cables.

#### Frame Relay
Connect LAN to WAN (internet).

> Internet is a collection of LANs, MANs, WANs. Connecting Local Area Networks to Wide Area Networks.

### Modem
Used to convert digital signals to analog signals and vice versa.

### Router
Routes the data packets based on their IP Addresses.

## Topologies

### Bus Topology
Every system connected to a Backbone cable.

```
    *        *
*------------------*
  *      *      *
```
CONS: 

- Backbone gets broken, all the systems are down.

- Only one system can transmit data at a time.


### Ring Topology

Every system communicates with one another.

```
    *  ---- *
  /            \  
*                *
 \              /
     * ---- *
```

CONS: 

- If one system fails, all the systems are down.

- Lot of unnecessary calls between systems.


### Star Topology

All computers connected to a central hub.

```
         *
         |
         |
  *----- * ------*
         |
         |
         *
```

CONS:

- If the hub fails, all the systems are down.

### Tree Topology (Combination of Bus and Star)

Many stars connected to a bus topology. 

```
         *
         |          *
         |         /
  *----- * ------* ---- *
         |        \
         |          *
         *
         |
         |
         *
        /  \
       *    *
```

PROS:

- More fault tolerance.

### Mesh Topology

Every system connected to every other system.

```
   *  ---- *  ---- *
   |     /       /
   |   /      /
   | /    /
   * /
```

CONS:

- Very expensive.
- Scalability is an issue.


# Structure of the Network

> Example:
You order food, restaurant sends the order to the kitchen, kitchen sends the order to the delivery guy, delivery guy delivers the food to you.

> Example:
You order something online. Amazon gets the order, sends the order to the delivery company, delivery company transports it. Arrived in India, assigns it to the delivery company resoponsible. Delivery company delivers the order to you.

This is how we can imagine internet.

The Application Layer is where you order stuff. (via application)


## OSI Model (Open Systems Interconnection Model)

This is how the internet works.

OSI Model is a standard model how two or more computers communicate with each other.

There are 7 layers in the OSI Model.

1. Application Layer
2. Presentation Layer
3. Session Layer
4. Transport Layer
5. Network Layer
6. Data Link Layer
7. Physical Layer

> Most important topic for interviews.

Every layer has different set of protocols and devices being used.

### Application Layer

Implemented in software. In the application (browser, messaging apps, etc.)

Send message to presentation layer.

**Application Layer Protocols**
- HTTP
- FTP
- SMTP
- DNS
- Telnet

### Presentation Layer

Takes the data from the application layer.

Data is in form of Words, Characters, Numbers, etc.
Presentation layer converts data into binary (machine readable format).

- From ASCII to EBCDIC.

- Called **Translation of data**.

- Goes under **Encoding** and **Encryption**, so that it is only readable to the person that the data was sent to.

- Also provides **Abstraction**.

Presentation layer assumes that if the data is sent downward, it will take care of it.

> Encryption, Compression, Translation.

**Presentation Layer Protocols**

- SSL (Secure Socket Layer) - For encryption decryption.

Data is sent to the session layer.

### Session Layer

Helps in setting up and managing the connections, including sending and receiving data, followed by termination of the session.

> Servers ask for username and password - that is **Authentication** - after that **Authorization** is done - Permission to access the data on the server.

Session layer assumes that if the data is sent downward, it will take care of it. (Basically all layers are independent of each other.)

### Transport Layer

Data is sent from the Session Layer to the Transport Layer.

Has UDP and TCP protocols to transfer data to another computer.

**TCP (Transmission Control Protocol)**
- Correction oriented transmission.
- TCP is slower than UDP.
- Sends acknowledgement to the sender to confirm that the data has been received.

**UDP (User Datagram Protocol)**
- Correction-less oriented transmission.
- UDP is faster than TCP.
- Data packets get lost or corrupted.
Doesn't perform error checking.
- Eg: Video streaming, Voice over IP.

Contains 3 steps:

#### 1. Segmentation 

- Data is broken into smaller chunks called **Segments**.

- Each segment has **source and destination's Port Number**, a **Sequence Number**.

- **Sequence Number** is used to reassemble the data in the correct order. (Chunks)

#### 2. Flow Control

- Transport layer controls the amount of data being transported.

> If server has 40mbps and client has 10mbps, then it wont work.

#### 3. Error Control

- Data packets got lost or corrupted.

- Adds **Checksum** to the data packets to see if data is good or not.


### Network Layer

Works for transmission of the received data segments from one computer to another. (Located in a different network)

- Router lies in the Network Layer.

**FUNCTIONS**:

- Logical addressing.
- Every computer has a unique IP Address. Network layer assigns the senders and receivers IP Addresses to every Segment. (Forms an IP Packet)
- Every data packet can reach its destination.
- Performs **Routing** - Decides the best path to reach the destination.
- **Load Balancing** - Divides the load between the servers. Makes sure that the servers are not overloaded.