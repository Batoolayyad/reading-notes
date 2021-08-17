## How do bearer tokens work?
Bearer Token A security token with the property that any party in possession of the token (a “bearer”) can use the token in any way that any other party in possession of it can. Using a bearer token does not require a bearer to prove possession of cryptographic key material (proof-of-possession).


## Describe express middleware
- The Bearer Token is created for you by the Authentication server. When a user authenticates your application (client) the authentication server then goes and generates for you a Token.

- The Bearer Token is normally some kind of opaque value created by the authentication server. It isn’t random; it is created based upon the user giving you access and the client your application getting access.

- To get an access token you send the Authentication server this bearer token along with your client id. This way the server knows that the application using the bearer token is the same application that the bearer token was created for.


## What is a JWT?
[ref](https://jwt.io/introduction) JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.


## Term


### role based access control
[ref](https://en.wikipedia.org/wiki/Role-based_access_control)
Role-based access control (RBAC) is a policy-neutral access-control mechanism defined around roles and privileges. The components of RBAC such as role-permissions, user-role and role-role relationships make it simple to perform user assignments. A study by NIST has demonstrated that RBAC addresses many needs of commercial and government organizations


### http cookies
[ref](https://en.wikipedia.org/wiki/HTTP_cookie) **http cookies**(also called web cookies, Internet cookies, browser cookies, or simply cookies) are small blocks of data created by a web server while a user is browsing a website and placed on the user's computer or other device by the user’s web browser. Cookies are placed on the device used to access a website, and more than one cookie may be placed on a user’s device during a session.

Cookies serve useful and sometimes essential functions on the web.