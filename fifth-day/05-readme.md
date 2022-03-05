# 05-03-2022- Fifth class reading notes:

## Securing Passwords with Bcrypt Hashing Function

Passwords are the first line of defense against cyber criminals. It is the most vital secret of every activity we do over the internet and also a final check to get into any of your user account, whether it is your bank account, email account, shopping cart account or any other account you have.

The benefit of hashing is that if someone steals the database with hashed passwords, they only make off with the hashes and not the actual plaintext passwords. But why do we always hear about passwords being cracked? There are some weaknesses in cryptographic hash algorithm that allows an attacker to calculate the original value of a hashed password, as explained below:

**PROBLEMS WITH CRYPTOGRAPHIC HASH ALGORITHM**

1. Brute Force attacker
2. Hash Collision attack
3. BCrypt, IT's SLOW AND STRONG AS HELL

## **Authentication Cheat Sheet**

Introduction
Authentication is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

Session Management is a process by which a server maintains the state of an entity interacting with it. This is required for a server to remember how to react to subsequent requests throughout a transaction. Sessions are maintained on the server by a session identifier which can be passed back and forward between the client and server when transmitting and receiving requests. Sessions should be unique per user and computationally very difficult to predict. The Session Management Cheat Sheet contains further guidance on the best practices in this area.


## Document the following Vocabulary Terms

- Router Middleware: A middleware is a function taking a router instance and registered dependencies (like lifecycle methods and plugins) and returning a function which will be called on each transition (unless a transition failed at the canActivate or canDeactivate state).

- Dynamic Module Loading:portable method for dynamically loading 'plug-ins'
  
- Singleton Pattern:s one of the simplest design patterns in Java. This type of design pattern comes under creational pattern as this pattern provides one of the best ways to create an object.

This pattern involves a single class which is responsible to create an object while making sure that only single object gets created. This class provides a way to access its only object which can be accessed directly without need to instantiate the object of the class.

- CRUD -> REST Method Matches:  operations are basic data manipulation for database.
  
- Mock Testing: is an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules.