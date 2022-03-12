# 20-2-2022- First class reading notes:

## Authorization/Authentication:

1. What header(s) are used in authentication and authorization
   The Authentication Header is also called as AH. It provides support for data integrity and authentication of IP data packets. Here data integrity ensures that the data that lies inside the IP packets are not altered during the transmission of packets, and Authentication services enable the user or computer system to authenticate the user to the application at other end and based on the result, it decides whether to allow or reject. An authentication header prevents the IP spoofing attack. In order to use AH, two parties must share the secret key for communication.
   it used to provide credentials that authenticate a user agent with a server and header is usually, but not always, sent after the user agent first attempts to request a protected resource without credentials.

2. What is safe to put into a JWT
   Iss– containing the username of the logged in user. This is especially useful since we might want to show that in our UI
   Exp– because we’ll only allow this new token to be used for the next 8 hours (which is usually how long users should be using it on a daily basis)
   Admin– boolean describing the role of the user. This comes in handy for the UI, since we’ll need to understand whether to show or hide some UI elements

3. How are JWTs validated
    To parse and validate a JSON Web Token (JWT), you can:
    - Use any existing middleware for your web framework.
    - Choose a third-party library from JWT.io.
    - Manually implement the checks described in specification RFC 7519 > 7.2 Validating a JWT.

    We strongly recommend that you use middleware or one of the existing open source third-party libraries to parse and validate JWTs. At JWT.io, you can find libraries for various platforms and languages, such as .NET, Python, Java, Ruby, Objective-C, Swift, and PHP.

## Document the following Vocabulary Terms
 **RBAC**: also known as role-based security, is an access control method that assigns permissions to end-users based on their role within your organization. RBAC provides fine-grained control, offering a simple, manageable approach to access management that is less error-prone than individually assigning permissions. 

 **User roles**: is a property of a BIG-IP® administrative user account. For each BIG-IP user account, you can assign a different user role to each administrative partition to which you the user has access. This allows you to assign multiple user roles to each user account on the system.

 **JWT Token**: is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.
