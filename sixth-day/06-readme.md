# 07-March-2022- Sixth class reading notes:

## Bearer Authorization:

### Review, Research, and Discussion:

1. What can you do with an authorization code?
   grant any transaction or entry that has restrictions on which users are entitled to access.
2. What can you do with an access token?
3. allow an application to access an API.
4. What’s a benefit of using OAuth instead of your own basic authentication?
5. provides applications the ability for “secure designated access.”

### Document the following Vocabulary Terms
Term: 
- Client ID: also referred to as a UCI, is on all documents you get from us. It is an eight or ten-digit number that looks like this: 0000-0000 or 00-0000-0000. If you are applying to us for the first time, you will not yet have a client ID.
  
- Client Secret: is a secret known only to your application and the authorization server. It protects your resources by only granting tokens to authorized requestors. 
  
- Authentication Endpoint:  is an authentication mechanism used to verify the identity of a network's external or remote connecting device. This method ensures that only valid or authorized endpoint devices are connected to a network.
  
- Access Token Endpoint: are the thing that applications use to make API requests on behalf of a user. The access token represents the authorization of a specific application to access specific parts of a user’s data.
  
- API Endpoint: is a digital location where an API receives requests about a specific resource on its server. 
  
- Authorization Code:  is typically a sequence of letters, numbers, or a combination of both, that validates a person's identity, approves a transaction or provides access to a secured area.
  
- Access Token: are used in token-based authentication to allow an application to access an API.

### Preview

#### What is JSON Web Token?
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

When should you use JSON Web Tokens?
Here are some scenarios where JSON Web Tokens are useful:

Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

What is the JSON Web Token structure?
In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

Header
Payload
Signature

#### Review questions
1. Which 3 things had you heard about previously and now have better clarity on? no one of them
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
3. Tokens and JWT
4. What are you most excited about trying to implement or see how it works? all of them