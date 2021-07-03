### Explain what a “Singleton” is (in Computer Science terms)
[techopedia](https://www.techopedia.com/definition/15830/singleton)


is a class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself. 


### Explain how the Singleton pattern can be used with Node modules, specifically with classes
[techopedia](https://www.techopedia.com/definition/15830/singleton)


to define a global variable. A single object used across systems remains constant and needs to be defined only once rather than many times.


## Term


### Router Middleware
[expressjs](https://expressjs.com/en/guide/using-middleware.html)
functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle.


### Dynamic Module Loading
[npmjs](https://www.npmjs.com/package/dynamic-module-loader/v/1.0.1)
library allows code to retrieve Node modules from a web server, install them locally and serve them up as though they'd been manually deployed to the running server


### Singleton Pattern
[wikipedia](https://en.wikipedia.org/wiki/Singleton_pattern)
is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system


### CRUD -> REST Method Matches


[restapitutorial](https://www.restapitutorial.com/lessons/httpmethods.html)
the most-commonly-used HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE. These correspond to create, read, update, and delete (or CRUD) operations, respectively.


### Mock Testing
[devopedia.org](https://devopedia.org/mock-testing) is an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules. In mock testing, the dependencies are replaced with objects that simulate the behaviour of the real ones. The purpose of mocking is to isolate and focus on the code being tested and not on the behaviour or state of external dependencies.


## Securing Passwords with Bcrypt Hashing Function
[thehackernews](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)


Many desktop applications and almost every web service including, blogs, forums eventually need to store a collection of user data and the passwords, that has to be stored using a hashing algorithm.
Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions, designed to calculate a digest of huge amounts of data in as short a time as possible. Hashing is the greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of data or password.
The benefit of hashing is that if someone steals the database with hashed passwords, they only make off with the hashes and not the actual plaintext passwords.


## Basic Auth
[wikipedia](https://en.wikipedia.org/wiki/Basic_access_authentication)


HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.


## OWASP auth cheatsheet
[OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)


- **Authentication** is the process of verifying that an individual, entity or website is whom it claims to be.

- **Session Management** is a process by which a server maintains the state of an entity interacting with it.

- **TLS Client Authentication**  also known as two-way TLS authentication, consists of both, browser and server, sending their respective TLS certificates during the TLS handshake process. 


- **Authentication and Error Messages**, Incorrectly implemented error messages in the case of authentication functionality can be used for the purposes of user ID and password enumeration. An application should respond (both HTTP and HTML) in a generic manner.

