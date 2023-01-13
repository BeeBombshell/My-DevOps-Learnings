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