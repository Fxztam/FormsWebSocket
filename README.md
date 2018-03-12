# FormsWebSocket
## 1. Overview
WebSocket provides an alternative to the limitation of efficient communication
between the server and the web browser by providing:

- bi-directional 
- full-duplex 
- real-time

client / server communications. 

The server can send data to the client at any time. Because it runs over TCP, it also provides a low-latency low-level communication and 
reduces the overhead of each message.
## 2. JSR 356
JSR 356 or the Java API for WebSocket, specifies an API that Java developers can use for integrating WebSockets withing their applications – both on the server side as well as on the Java client side.

This Java API provides both server and client side components:

- Server: everything in the javax.websocket.server package.
- Client: the content of javax.websocket package, which consists of client side APIs and also common libraries to both server and client.
