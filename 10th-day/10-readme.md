# 15-March-2022- 10th class reading notes:

## Event Driven Applications:

 is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision. In this article we’re going to go over how Event-Driven Programming works and how we can make the best use of it in our Node.js projects.

**Event-Driven Programming makes use of the following concepts:**

 An Event Handler is a callback function that will be called when an event is triggered.
 A Main Loop listens for event triggers and calls the associated event handler for that event.

 **EventEmitter** that allows us to get started incorporating Event-Driven Programming in our project right away.
 All EventEmitters emit the event 'newListener' when new listeners are added and 'removeListener' when existing listeners are removed.

It supports the following option:

captureRejections <boolean> It enables automatic capturing of promise rejection. Default: false.

The EventEmitter instance will emit its own 'newListener' event before a listener is added to its internal array of listeners.

Listeners registered for the 'newListener' event are passed the event name and a reference to the listener being added.

The fact that the event is triggered before adding the listener has a subtle but important side effect: any additional listeners registered to the same name within the 'newListener' callback are inserted before the listener that is in the process of being added.

Asynchronous vs. synchronous#
The EventEmitter calls all listeners synchronously in the order in which they were registered. This ensures the proper sequencing of events and helps avoid race conditions and logic errors. When appropriate, listener functions can switch to an asynchronous mode of operation using the setImmediate() or process.nextTick() methods:

### Review, Research, and Discussion

1. Why is access control important?
   ccess control is important because it is a valuable security technique that can be used to regulate who or what can view or use any given resource. In an I.T security setting this could translate to who can access and edit a particular file, what kinds of equipment can be used or who can access certain devices.

2. Why is role based access control more scalable than discretionary or mandatory access control?
   regulates which users, applications, and devices can view, edit, add, and delete resources in an organization’s environment. Controlling access is one of the key practices to protect sensitive data from theft, misuse, abuse, and any other threats. There are two levels of access control: physical and logical.
   There are several logical access control models: mandatory, discretionary, role-based, attribute-based, etc. The process of choosing and deploying an access control model looks different for each organization. This choice depends on:

    1. The nature of the protected data
    2. IT requirements and industry standards
    3. The number of employees
    4. The cybersecurity budget


Mandatory access control (MAC) is a model of access control where the operating system provides users with access based on data confidentiality and user clearance levels. In this model, access is granted on a need to know basis: users have to prove a need for information before gaining access.

#### Document the following Vocabulary Terms

- **Authorization**: Authorization is the function of specifying access rights/privileges to resources, which is related to general information security and computer security, and to access control in particular. More formally, "to authorize" is to define an access policy.
  
- **Role Based Access Control**: is an approach to restricting system access to authorized users. It is an approach to implement mandatory access control (MAC) or discretionary access control (DAC).
  
- **Capabilities**: is a concept in the design of secure computing systems, one of the existing security models. A capability (known in some systems as a key) is a communicable, unforgeable token of authority. It refers to a value that references an object along with an associated set of access rights. 