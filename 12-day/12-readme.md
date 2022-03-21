# 21-March-2022- 12th class reading notes:

## Message Queues:

**Introduction**
Writing a chat application with popular web applications stacks like LAMP (PHP) has normally been very hard. It involves polling the server for changes, keeping track of timestamps, and it’s a lot slower than it should be.

Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server.

**Serving HTML**
So far in index.js we’re calling res.send and passing it a string of HTML. Our code would look very confusing if we just placed our entire application’s HTML there, so instead we're going to create a index.html file and serve that instead.

**Integrating Socket.IO**
Socket.IO is composed of two parts:

A server that integrates with (or mounts on) the Node.JS HTTP Server socket.io
A client library that loads on the browser side socket.io-client

**Emitting events**
The main idea behind Socket.IO is that you can send and receive any events you want, with any data you want. Any objects that can be encoded as JSON will do, and binary data is supported too.


**Broadcasting**
The next goal is for us to emit the event from the server to the rest of the users.

In order to send an event to everyone, Socket.IO gives us the io.emit() method.

io.emit('some event', { someProperty: 'some value', otherProperty: 

### **Key features of WebSocket**

    1. What does it mean that web sockets are bidirectional? Why is this useful?
    means the data incoming and outgoing data flows over the same channel (sockets), in classical socket it is the case. For example you want to connect to a server: you create a socket, send and receive the data over the same channel.

    1. Does socket.io use HTTP? Why?
    Even when websockets can be used, the initial connection setup it done over HTTP. Also, a socket.io server will attach to an HTTP server so it can serve its own client code through /socket.io/socket.io.js.

    That said, although you don't need an HTTP server to regular websockets, there's no denying that the websocket protocol was designed with HTTP in mind (as to allow HTTP and websocket servers to co-exist on the same TCP port).

    1. What happens when a client emits an event?
     this means that you can listen for its event and add additional logic to your code, without need to change the client internals or your normal usage. You can find the events names by access the events key of the client.

    2. What happens when a server emits an event?
     Server emits an event of connection as soon as a socket gets connected to server, this event then triggers the parent function of getConnections, which indeed also takes a call-back function as argument. So, it indeed is a chain, which is triggered as something happens by event emitter which emits an event to start a function running.
   

### Document the following Vocabulary Terms

- Socket:  is used in a client-server application framework. A server is a process that performs some functions on request from a client.
- Web Socket: is a computer communications protocol, providing full-duplex communication channels over a single TCP connection.
- Socket.io:  is a JavaScript library for realtime web applications. It enables realtime, bi-directional communication between web clients and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for Node.js. 
- Client:  which means the source code is processed by the client's web browser rather than on the web server. This means JavaScript functions can run after a webpage has loaded without communicating with the server.
- Server: is a piece of computer hardware or software (computer program) that provides functionality for other programs or devices, called "clients". This architecture is called the client–server model. Servers can provide various functionalities, often called "services"
- OSI Model: The Open Systems Interconnection model (OSI model) is a conceptual model that characterises and standardises the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology. Its goal is the interoperability of diverse communication systems with standard communication protocols.
- TCP Model:  is the set of communications protocols used in the Internet and similar computer networks. The current foundational protocols in the suite are the Transmission Control Protocol (TCP) and the Internet Protocol (IP).
- TCP: The Transmission Control Protocol (TCP) is one of the main protocols of the Internet protocol suite. It originated in the initial network implementation in which it complemented the Internet Protocol (IP). Therefore, the entire suite is commonly referred to as TCP/IP.
- UDP: User Datagram Protocol (UDP) is a Transport Layer protocol. UDP is a part of the Internet Protocol suite, referred to as UDP/IP suite. Unlike TCP, it is an unreliable and connectionless protocol. So, there is no need to establish a connection prior to data transfer. 
- Packets: is a formatted unit of data carried by a packet-switched network. A packet consists of control information and user data; the latter is also known as the payload. 