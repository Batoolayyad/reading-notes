## What is the benefit of transforming data into packets?
[premieritsolution](https://premieritsolution.co.uk/the-important-of-access-control/)
Access control is important because it is a valuable security technique that can be used to regulate who or what can view or use any given resource. 


## UDP is often refereed to as a connectionless protocol. Why is this?
[oracle](https://docs.oracle.com/cd/E19620-01/805-4041/6j3r8iu2f/index.html#:~:text=UDP%20is%20a%20connectionless%20protocol,services%20are%20broadcasting%20and%20tftp%20.)
UDP is a connectionless protocol. It is known as a datagram protocol because it is analogous to sending a letter where you don't acknowledge receipt.

## Can a socket server application have multiple socket connections?
[stackoverflow](https://stackoverflow.com/questions/60653131/maximum-number-of-socket-for-http-traffic-connections-possible-for-a-single-ma)
yes,65535 is the maximum number of TCP ports available.


## Can a socket connection application be connected to multiple socket servers?


Yes, each listening (bound) port is serviced by a separate socket (as are all the connections made from each listening port)


## Can an application be both a socket server and a socket connection?
yes



## Term


### Observer Pattern:
[wikipedia](https://en.wikipedia.org/wiki/Observer_pattern)
The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.


### Listener
[computerhope](https://www.computerhope.com/jargon/e/event-listener.htm)
 event listener is a procedure or function in a computer program that waits for an event to occur. Examples of an event are the user clicking or moving the mouse, pressing a key on the keyboard, disk I/O, network activity, or an internal timer or interrupt. The listener is programmed to react to an input or signal by calling the event's handler.


### Event Handler
[computerhope](https://www.computerhope.com/jargon/e/event-listener.htm)
 subroutine that performs a similar function


### Event Driven Programming
[ref](https://brainly.in/question/29629003)

event-driven programming is when a program is designed to respond to user engagement in various forms. It is known as a programming paradigm in which the flow of program execution is determined by “events.”


### Event Loop
[nodejs.org](https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/)
 is what allows Node.js to perform non-blocking I/O operations — despite the fact that JavaScript is single-threaded — by offloading operations to the system kernel whenever possible.


### Event Queue
[ref](https://www.techopedia.com/definition/24963/event-queue#:~:text=An%20event%20queue%20is%20a,of%20an%20enterprise%20messaging%20system.)
is a repository where events from an application are held prior to being processed by a receiving program or system


### Call Stack
[ref](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)
 call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions 


### Emit/Raise/Trigger
[ref](https://stackabuse.com/handling-events-in-node-js-with-evenemitter)
object which will emit an event that contains information about the application's uptime, every second.


### Subscribe
Subscribes an event handler method or procedure to an ABL or .NET class event.


### database
[ref](https://towardsdatascience.com/web-scraping-basics-82f8b5acd45c)
structured way to store data locally so as to not make repetive requests/receive repetitive responses.


## WebSocket
[wikipedia](https://en.wikipedia.org/wiki/WebSocket)
WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. 

##### Protocol handshake

To establish a WebSocket connection, the client sends a WebSocket handshake request, for which the server returns a WebSocket handshake response, as shown in the example below.


- Client request (just like in HTTP, each line ends with \r\n and there must be an extra blank line at the end):
```
GET /chat HTTP/1.1
Host: server.example.com
Upgrade: websocket
Connection: Upgrade
Sec-WebSocket-Key: x3JJHMbDL1EzLkh9GBhXDw==
Sec-WebSocket-Protocol: chat, superchat
Sec-WebSocket-Version: 13
Origin: http://example.com
```


- Server response:
```
HTTP/1.1 101 Switching Protocols
Upgrade: websocket
Connection: Upgrade
Sec-WebSocket-Accept: HSmrc0sMlYUkAGmm5OPpG2HaGWk=
Sec-WebSocket-Protocol: chat
```


#### Security considerations

Unlike regular cross-domain HTTP requests, WebSocket requests are not restricted by the Same-origin policy. but  servers must validate the "Origin" header against the expected origins during connection establishment, to avoid Cross-Site WebSocket Hijacking attacks (similar to Cross-site request forgery), which might be possible when the connection is authenticated with Cookies or HTTP authentication. It is better to use tokens or similar protection mechanisms to authenticate the WebSocket connection when sensitive (private) data is being transferred over the WebSocket. 


## Socket
[socket.io](https://www.tutorialspoint.com/socket.io/)


Socket.IO enables real-time bidirectional event-based communication. It works on every platform, browser or device, focusing equally on reliability and speed. Socket.IO is built on top of the WebSockets API (Client side) and Node.js. It is one of the most depended upon library on npm (Node Package Manager).


#### what is the difference Between WebSocket and Socket.io
- **WebSocket** is the communication Protocol that provides bidirectional communication between the Client and the Server over a TCP connection; WebSocket remains open all the time, so they allow real-time data transfer. When clients trigger the request to the server, it does not close the connection on receiving the response; it rather persists and waits for the Client or server to terminate the request.

- **Socket.IO** is a library that enables real-time and full-duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts; both WebSocket vs Socket.io are event-driven libraries.


### Terms

- Client-Side: it is the library that runs inside the browser
- Server Side: It is the library for Node.js
WebSocket
Below are the features:


#### Why do we need Socket.IO:
- I handle all the degradation of your technical alternatives to get full-duplex communication in real-time.
- It also handles the various support level and the inconsistencies from the browser.
- It also gives the additional feature room support for basic publish infrastructure and thinks like automatic reconnect.
- Currently, AFAIK is the most used one and easier to help with vanilla web sockets.