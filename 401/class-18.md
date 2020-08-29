# Sockets.io

-  What is the benefit of transforming data into packets?
  >  Standardizing information.  
-  UDP is often refereed to as a connectionless protocol. Why is this?
  >   UDP doesn't establish a connection before sending data, it just sends. Because of this, UDP is called "Connectionless". UDP packets are often called "Datagrams". ... DNS servers send and receive DNS requests using UDP
- Can a socket server application have multiple socket connections?
  > A server socket listens on a single port. All established client connections on that server are associated with that same listening port on the server side of the connection. An established connection is uniquely identified by the combination of client-side and server-side IP/Port pairs. Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs, and the server would be able to handle as many clients as available system resources allow it to.

  On the client-side, it is common practice for new outbound connections to use a random client-side port, in which case it is possible to run out of available ports if you make a lot of connections in a short amount of time.

- Can an application be both a socket server and a socket connection?
  > you can send and receive at the same time. What you can't have is two threads sending over the same TCP/IP socket or two threads receiving at the same TCP/IP socket

***
### Terms
1. OSI Model -  the communications between a computing system are split into seven different abstraction layers; 
  > Physical, Data Link, Network, Transport, Session, Presentation, and Application.
1. TCP Model -  unlike the OSI model this is split into four different layers;
  > Process/Application Layer
Host-to-Host/Transport Layer
Internet Layer
Network Access/Link Layer
1. TCP - is an important network protocol that lets two hosts connect and exchange data streams. TCP guarantees the delivery of data and packets in the same order as they were sent
1. UDP -  is a long standing protocol used together with IP for sending data when transmission speed and efficiency matter more than security and reliability. UDP uses a simple connectionless communication model with a minimum of protocol mechanism
1. Packets -  is a formatted chunk of data sent over a network. The maincomponents of a network packet are the user data and control information. The user data is known as the payload. The control information is the information for delivering the payload
1. Socket - is a JavaScript library for realtime web applications. It enables realtime, bi-directional communication between web clients and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for Node. js.

*** 
### Resources 

1. [Resource 1](https://en.wikipedia.org/wiki/WebSocket)
1. [Resource 2](https://www.tutorialspoint.com/socket.io/)
1. [Resource 3](https://www.educba.com/websocket-vs-socket-io/)
1. [Resource 4](https://socket.io/docs/)
1. [Resource 5](https://socket.io/docs/server-api)
1. [Resource 6](https://socket.io/docs/client-api)
1. [Resource 7](https://amritb.github.io/socketio-client-tool/)
