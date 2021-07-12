## What does it mean that web sockets are bidirectional? Why is this useful?

it gose into two directions (client request to receive a response from the server for every exchange). This enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time.

## Does socket.io use HTTP? Why?
yes,  

## What happens when a client emits an event?
[ref](https://stackoverflow.com/questions/48332454/how-does-socket-io-on-the-client-listen-to-events-emitted-from-server)
The event gets passed to the server through websockets. Its a tcp connection from the browser to the server. The connection is full duplex meaning the server can send real time data to the client and vise versa.

In your frontend code you should have something that looks similar to
```
<script src="/socket.io/socket.io.js"></script>
<script>
  var socket = io();
</script>
```
This code asks the server for a tcp connection using web sockets. Once the browser is connected to the server through websockets, socket.io can send events to the send through the connection.

The socket that is passed in the connection event is just a reference to whatever socket gets created when the frontend connects. The socket gets a unique id and with this reference you can communicate in real time to the web browser client.


## What happens when a server emits an event?

All listening client will execute the handeler for that event.


## What happens if a client “misses” an event?

the handler woudln’t be executed.


## How can we mitigate this?

we can push a missed event to the Buffers until it is used.


## Document the following Vocabulary Terms

## Term

#### Socket
[ref](https://docs.oracle.com/javase/tutorial/networking/sockets/definition.html)
A socket is one endpoint of a two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to.


#### Web Socket
[ref](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)
 is an advanced technology that makes it possible to open a two-way interactive communication session between the user's browser and a server. 


#### Socket.io:
[ref](https://stackoverflow.com/questions/37836130/socket-io-why-does-it-need-an-http-server#:~:text=Also%2C%20a%20socket.io%20server,%2Fsocket.io.js%20.)
It's a real time, bidirectional event-based communication library 


#### Client
in the side that receive the data that the server provied it with
#### Server
[ref](https://www.paessler.com/it-explained/server)
is a computer or system that provides resources, data, services, or programs to other computers, known as clients, over a network. In theory, whenever computers share resources with client machines they are considered servers.


#### OSI Model
[ref](https://www.forcepoint.com/cyber-edu/osi-model)
The OSI Model (Open Systems Interconnection Model) is a conceptual framework used to describe the functions of a networking system.


#### TCP Model
is a concise version of the OSI model,  It contains four layers, unlike seven layers in the OSI model. The layers are:
Process/Application Layer,
Host-to-Host/Transport Layer,
Internet Layer,
Network Access/Link Layer,
#### TCP
[ref](https://www.fortinet.com/resources/cyberglossary/tcp-ip)
Transmission Control Protocol a communications standard that enables application programs and computing devices to exchange messages over a network. It is designed to send packets across the internet and ensure the successful delivery of data and messages over networks.


#### UDP
[ref](https://searchnetworking.techtarget.com/definition/UDP-User-Datagram-Protocol)
UDP (User Datagram Protocol) is a communications protocol that is primarily used for establishing low-latency and loss-tolerating connections between applications on the internet. It speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party


#### Packets
[ref](https://en.wikipedia.org/wiki/Network_packet)
is a formatted unit of data carried by a packet-switched network. A packet consists of control information and user data;[1] the latter is also known as the payload. 


## Socket.io Chat Example
[socket.io](https://socket.io/get-started/chat/)
Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server.

This means that the server can push messages to clients. Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients.

notes:

- in the clint side we dont specifying any URL when I call io(), since it defaults to trying to connect to the host that serves the page.(var socket = io();)

- Each socket fires a special disconnect event:
```
io.on('connection', (socket) => {
  console.log('a user connected');
  socket.on('disconnect', () => {
    console.log('user disconnected');
  });
});
```
- socket io allowed you to send and receive any events you want, with any data you want.

- in order to send an event to everyone, Socket.IO gives us the io.emit() method

- If you want to send a message to everyone except for a certain emitting socket, we have the broadcast flag for emitting from that socket:

```
io.on('connection', (socket) => {
  socket.broadcast.emit('hi');
});
```

## Rooms

- A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients
- rooms are a server-only concept (i.e. the client does not have access to the list of rooms it has joined).

- You can call join to subscribe the socket to a given channel:
```
io.on('connection', socket => {
  socket.join('some room');
});
```
- And then simply use to or in (they are the same) when broadcasting or emitting:
```
io.to('some room').emit('some event');
```

- Socket in Socket.IO is identified by a random, unique identifier Socket#id.

- You can fetch the rooms the Socket was in by listening to the disconnecting event:
```
io.on('connection', socket => {
  socket.on('disconnecting', () => {
    console.log(socket.rooms); // the Set contains at least the socket ID
  });

  socket.on('disconnect', () => {
    // socket.rooms.size === 0
  });
});
```