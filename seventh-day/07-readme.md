# 09-March-2022- Seventh class reading notes:

## Access Control (ACL):

**role-based access control (RBAC) or role-based security**
 is an approach to restricting system access to authorized users. It is an approach to implement mandatory access control (MAC) or discretionary access control (DAC).

Role-based access control (RBAC) is a policy-neutral access-control mechanism defined around roles and privileges. The components of RBAC such as role-permissions, user-role and role-role relationships make it simple to perform user assignments. A study by NIST has demonstrated that RBAC addresses many needs of commercial and government organizations.[4] RBAC can be used to facilitate administration of security in large organizations with hundreds of users and thousands of permissions. Although RBAC is different from MAC and DAC access control frameworks, it can enforce these policies without any complication.

### RBAC definition

RBAC is the idea of assigning system access to users based on their role within an organization. The system needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and system access needs. Access is then assigned to each person based strictly on their role assignment. With tight adherence to access requirements established for each role, access management becomes much easier.

**Benefits of RBAC**
With the proper implementation of RBAC, the assignment of access rights becomes systematic and repeatable. Further, it is much easier to audit user rights, and to correct any issues identified.

RBAC may sound intimidating, but it can in reality be easy to implement, and will make the ongoing management of access rights much easier and more secure.

The data breach you prevent may be your own.

### Review, Research, and Discussion:

1. When is Basic Authorization used vs. Bearer Authorization?
   
**Basic Auth**
The basis Auth allow you to access the API directly with your credential : user/password.
Use case
The use case for this are integration with reporting tools like PowerBI, Tableau, QLik, BoldBI.

**How to use it**

1. For instance, in Postman when calling the API choose "Basic Auth" and fill-in the user password. The information will be encoded with Base64 to avoid to be readable when sent. 
2. For instance, in a script in curl add the header Authorization: Basic and pass the encoded value of the login and password.
This authentication method is useful when you need to check identity and get the data in one call. In the back end the server will generate a bearer token that will then be used to get the data.

**Bearer Token**
 

To access the API with a bearer token you will need to make 2 call :

one to get the bearer token
one to get the data
Once you have the bearer token you can reuse it and keep it for up to 60 minutes. You can refresh (to extend the validity) or revoke the bearer (to remove the validity) if needed.

Use case
It is the recommended Authentication methods whenever possible. It is ideal when scripting, when developing external app or when doing integration with external tools.

How to use it

1. Make a first call to the UAS endpoint to get a bearer. How to get a bearer Token 
2. Make a call to the API with the retrieve bearer.

- For instance, in Postman when calling the API choose "Bearer Token" and fill-in the bearer value. 
- For instance, in a script in curl add the header Authorization: Bearer and pass the value of the bearer.

2. What does the JSON Web Token package do?
 is JSON Object which is used to securely transfer information over the web (between two parties). It can be used for an authentication system and can also be used for information exchange.The token is mainly composed of header, payload, signature. These three parts are separated by dots (.).

3. What considerations should we make when creating and storing a SECRET?
   - Never store unencrypted secrets in .git repositories
   - Don’t share your secrets unencrypted in messaging systems like slack
   - Store secrets safely
     - Use encryption to store secrets within .git repositories
     - Use environment variables
     - Use "Secrets as a service" solutions
   - Restrict API access and permissions
     - Default to minimal permission scope for APIs
     - Whitelist IP addresses where appropriate
     - Use short-lived secrets


### Document the following Vocabulary Terms:

**Term:**

- encryption:is the process of encoding information. This process converts the original representation of the information, known as plaintext, into an alternative form known as ciphertext. Ideally, only authorized parties can decipher a ciphertext back to plaintext and access the original information.
  
- token:is an easy way to secure an API. When a user authenticates first on a server, using for instance a standard login form, the server creates a token. This token includes some personal data, such as username or email address. Then, this token is signed server-side (to prevent token integrity), and sent back to the user. Within each next request, user sends the token to establish emitter identity.
  
- bearer:is a cryptic string typically generated by the server in response to a login request. 
  
- secret:
- JSON Web Token:JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

### Preview:

1. Which 3 things had you heard about previously and now have better clarity on?
   the idea of authorization, authentaction and the time out of sessions.

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
   learning more about security and safety of the web application. 

3. What are you most excited about trying to implement or see how it works?
   the tokens and try another libraries.