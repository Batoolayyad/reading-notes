## When is Basic Authorization used vs. Bearer Authorization?


[ref](https://stackoverflow.com/questions/34013299/web-api-authentication-basic-vs-bearer)
- **The Basic** and Digest authentication schemes are dedicated to the authentication using a username and a secret 
- **The Bearer** authentication scheme is dedicated to the authentication using a token and is described


## What does the JSON Web Token package do?


[jwt.io](https://jwt.io/introduction)
that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.


## What considerations should we make when creating and storing a SECRET?


- Don't store them in .git repositories
- Add sensitive files in .gitignore
- Never rely on code reviews to discover secrets
- Encryptions should be used to store those secretes within .git repositories


## Document the following Vocabulary Terms
### Term
#### encryption:

[ref](https://searchsecurity.techtarget.com/definition/encryption#:~:text=Encryption%20is%20the%20method%20by,encrypted%20data%20is%20called%20ciphertext.)
 the method by which information is converted into secret code that hides the informations true meaning


#### token


coded string used to securely transfer information over the web.



#### bearer


[ref](https://oauth.net/2/bearer-tokens/)
Bearer Tokens are the predominant type of access token used with OAuth 2.0.
A Bearer Token is an opaque string, not intended to have any meaning to clients using it. Some servers will issue tokens that are a short string of hexadecimal characters, while others may use structured tokens such as JSON Web Tokens.


#### secret


Secret refers to a secret key or passcode that is used by a user to login, or create a login. A secret should be safeguarded by the user and additionally it should be encrypted


#### JSON Web Token



JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. 


## 5 steps to simple role-based access control (RBAC)

[5 steps to simple role-based access control (RBAC)](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)


### what is RBAC?
 is the idea of assigning system access to users based on their role in an organization. It's important to remember that not every employee needs a starring role.


### what Benefits of RBAC?


it can in reality be easy to implement, and will make the ongoing management of access rights much easier and more secure.


### RBAC implementation:


1- Inventory your systems 2- Analyze your workforce and create roles 3- Assign people to roles
4- Never make one-off changes 5- Audit



## RBAC


### what is the RBAC?
[wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)
Role-based access control (RBAC) is a policy-neutral access-control mechanism defined around roles and privileges. The components of RBAC such as role-permissions, user-role and role-role relationships make it simple to perform user assignments.

