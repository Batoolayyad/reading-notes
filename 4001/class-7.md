### Write the following steps in the correct order:


1- Ask the client if they want to sign in via a third party
2- Request a third-party API endpoint
3- Redirect to a third party authentication endpoint
4- Register your application to get a client_id and client_secret
5- Receive authorization code
6- Receive access token
7- Request the access token endpoint


### What can you do with an authorization code?


[investopedia](https://www.investopedia.com/terms/a/authorization-code.asp)
that authorizes its user to purchase, sell or transfer items, or to enter information into a security-protected space



### What can you do with an access token?


 applications use to make API requests on behalf of a user.


### What’s a benefit of using OAuth instead of your own basic authentication?


[clowder](https://www.clowder.com/post/why-your-organization-should-be-using-oauth-2.0)
1- It allows you to read data of a user from another application.
2- It supplies the authorization workflow for web, desktop applications, and mobile devices.
3- Is a server side web app that uses authorization code and does not interact with user credentials.
4- It gives users more control over their data; they can selectively grant access to various functionalities for applications they want to use.



## Term


#### Client ID


[oauth](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)
The client_id is a public identifier for apps. Even though it’s public, it’s best that it isn’t guessable by third parties, so many implementations use something like a 32-character hex string. It must also be unique across all clients that the authorization server handles. If the client ID is guessable, it makes it slightly easier to craft phishing attacks against arbitrary applications.


#### Client Secret


[oauth](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)
client_secret is a secret known only to the application and the authorization server. It must be sufficiently random to not be guessable, which means you should avoid using common UUID libraries which often take into account the timestamp or MAC address of the server generating it. A great way to generate a secure secret is to use a cryptographically-secure library to generate a 256-bit value and converting it to a hexadecimal representation.




#### Authentication Endpoint


It is a security mechanism designed to ensure that only authorized devices can connect to a given network, site or service.


#### Access Token Endpoint
[oauth](https://www.oauth.com/oauth2-servers/access-tokens/)
 token endpoint is where apps make a request to get an access token for a user
#### API Endpoint


[smartbear](https://smartbear.com/learn/performance-monitoring/api-endpoints/)
 Each endpoint is the location from which APIs can access the resources they need to carry out their function.



#### Authorization Code


[oauth](https://www.oauth.com/oauth2-servers/access-tokens/authorization-code-request/)
The authorization code grant is used when an application exchanges an authorization code for an access token. After the user returns to the application via the redirect URL, the application will get the authorization code from the URL and use it to request an access token. This request will be made to the token endpoint.


#### Access Token
[oauth](https://www.oauth.com/oauth2-servers/access-tokens/)
the thing that applications use to make API requests on behalf of a user. The access token represents the authorization of a specific application to access specific parts of a user’s data.



## JSON Web Token
[jwt](https://jwt.io/introduction/)
### What is JSON Web Token?


JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

### When should you use JSON Web Tokens?

- **Authorization**: Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token.

- **Information Exchange**:  good way of securely transmitting information between parties.

### What is the JSON Web Token structure?
- Header
- Payload
- Signature


## If you can decode JWT, how are they secure?
[If you can decode JWT, how are they secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)
WTs can be either signed, encrypted or both. If a token is signed, but not encrypted, everyone can read its contents, but when you don’t know the private key, you can’t change it. Otherwise, the receiver will notice that the signature won’t match anymore.

to understand digital signatures? I’ll just briefly explain one variant (HMAC, which is symmetrical, but there are many others).

Let’s assume Alice wants to send a JWT to Bob. They both know some shared secret. Mallory doesn’t know that secret, but wants to interfere and change the JWT. To prevent that, Alice calculates Hash(payload + secret) and appends this as signature.

When receiving the message, Bob can also calculate Hash(payload + secret) to check whether the signature matches. If however, Mallory changes something in the content, she isn't able to calculate the matching signature (which would be Hash(newContent + secret)). She doesn't know the secret and has no way of finding it out. This means if she changes something, the signature won't match anymore, and Bob will simply not accept the JWT anymore.

Let's suppose, I send another person the message {"id":1} and sign it with Hash(content + secret). (+ is just concatenation here). I use the SHA256 Hash function, and the signature I get is: 330e7b0775561c6e95797d4dd306a150046e239986f0a1373230fda0235bda8c. Now it's your turn: play the role of Mallory and try to sign the message {"id":2}. You can't because you don't know which secret I used. If I suppose that the recipient knows the secret, he CAN calculate the signature of any message and check if it's correct.


