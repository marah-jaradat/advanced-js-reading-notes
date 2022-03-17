# 17-March-2022- 11th class reading notes:

## Socket.io:

**WebSocket** is the communication Protocol that provides bidirectional communication between the Client and the Server over a TCP connection; WebSocket remains open all the time, so they allow real-time data transfer. When clients trigger the request to the server, it does not close the connection on receiving the response; it rather persists and waits for the Client or server to terminate the request.

**Key features of WebSocket**

    1. WebSocket helps in real-time communication between the Client and the webserver.
    2. This protocol helps in transforming to cross-platform in a real-time world between the server and the client.
    3. This also enables the business worldwide for a real-time web application to enhance and increase the feasibility.
    4. The major advantage it stands over an HTTP connection that it provides full-duplex communication.

**Why do we need WebSocket?**

    1. It provides full-duplex communication, which helps in persisting the connection established between the Client and the Web Server.
    2. It also lives up to the standards and provides the accuracy and efficiency stream events to and from with negligible latency.
    3. WebSocket removes the overhead and reduce complexity.
    4. It makes real-time communication effortless and efficient.

**Socket.IO** is a library that enables real-time and full-duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts; both WebSocket vs Socket.io are event-driven libraries.

Client-Side: it is the library that runs inside the browser
Server Side: It is the library for Node.js

**Key features of Socket.IO**

    1. It helps in broadcasting to multiple sockets at a time and handles the connection transparently.
    2. It works on all platform, server or device, ensuring equality, reliability, and speed.
    3. It automatically upgrades the requirement to WebSocket if needed.
    4. It is a custom real-time transport protocol implementation on top of other protocols.
    5. It requires both libraries to be used Client side as well as a server-side library.
    6. IO works on work-based events. there are some reserved events that can be accessed using the Socket on the server side like Connect, message, Disconnect, Ping and Reconnect.
    7. There are some Client based reserved events like Connect, connect- error, connect-timeout and Reconnect etc.

**Why do we need Socket.IO:**

    1. Io handle all the degradation of your technical alternatives to get full-duplex communication in real-time.
    2. It also handles the various support level and the inconsistencies from the browser.
    3.It also gives the additional feature room support for basic publish infrastructure and thinks like automatic reconnect.
    4. Currently, AFAIK is the most used one and easier to help with vanilla web sockets.

**Key Differences between WebSocket and socket.io**

Both WebSocket vs Socket.io are popular choices in the market; let us discuss some of the major Difference Between WebSocket vs Socket.io:

1. It provides the Connection over TCP, while Socket.io is a library to abstract the WebSocket connections.
2. WebSocket doesn’t have fallback options, while Socket.io supports fallback.
3. WebSocket is the technology, while Socket.io is a library for WebSockets.

### Review, Research, and Discussion

1. What is the benefit of transforming data into packets?
   In such cases, data is simply transmitted as an array of bytes or characters etc over the medium. Anyway, transformation of data into packets is a good way to achieve better bitrate of a communication medium in the course of sharing data amongst the users.

2. UDP is often refereed to as a connectionless protocol. Why is this?
    UDP is a connectionless protocol because different tasks require different solutions. It is the requirements you set for transporting a certain type of data that will decide wich protocols of TCP/IP is best. For example lets say you want to send a long news article containing text images and layout. That will most likely favor TCP with HTTP on top.

3. Can a socket server application have multiple socket connections?
   It is possible to have multiple TCP sockets listen on the same port number. There is a caveat to this though, each socket on the same server listening on the same port number must be associated with a different IP address.
   
4. Can a socket connection application be connected to multiple socket servers?
    multiple client sockets can be bound to the same local IP/port pair at the same time, if they are connected to different server IP/Port pairs so the tuples of local+remote pairs are unique. And yes, it is possible for a client to have more than 64K concurrent connections total.



### Document the following Vocabulary Terms

- **Observer Pattern**: The observer pattern is a software design pattern in    which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.
  
- **Listener**: is a method in JavaScript which waits for an event to take place. Event Listeners, also known as Event Handlers, where we can assign event listeners to particular events on a particular element. Event Listener is an interface representing an object that handles events dispatched by Event Object. Events are an important part of JavaScript as web pages respond based on the events. Some Events are user-generated, and some being generated by API calls. In this topic, we are going to learn about Javascript Event Listener.
  
- **Event Handler**: is a routine that deals with the event, allowing a programmer to write code that is executed when the event occurs. A web browser completely loading a web page.
  
- **Event Driven Programming**: is a computer programming paradigm where control flow of the program is determined by the occurrence of events. These events are monitored by code known as an event listener.
  
- **Event Loop**: s a programming construct or design pattern that waits for and dispatches events or messages in a program. The event loop works by making a request to some internal or external "event provider" (that generally blocks the request until an event has arrived), then calls the relevant event handler ("dispatches the event"). The event loop is also sometimes referred to as the message dispatcher, message loop, message pump, or run loop.
  
- **Event Queue**:  is a repository where events from an application are held prior to being processed by a receiving program or system. Event queues are often used in the context of an enterprise messaging system.
  
- **Call Stack**:  is a stack data structure that stores information about the active subroutines of a computer program. 
  
- **Emit/Raise/Trigger**:  can be raised at any point by a component. Typically it is raised by a user interaction, by clicking a button or selecting a row in a table. However, the component can raise the trigger based on any criteria; for example, when data changes because of a REST call.
  the difference between emit and trigger is that emit is while trigger is to fire a weapon.

- **database**:  is an organized collection of structured information, or data, typically stored electronically in a computer system. A database is usually controlled by a database management system (DBMS). Together, the data and the DBMS, along with the applications that are associated with them, are referred to as a database system, often shortened to just database.