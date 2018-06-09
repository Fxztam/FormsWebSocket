# FormsWebSocket
## 1. Overview
WebSocket is an Internet protocol providing two-way communication between a client and a server. WebSocket was designed to be implemented in web browsers ( https://caniuse.com/#feat=websockets) and web servers, but it can be used by any client or server application.
Messages can be delivered in either UTF-8 TEXT or BINARY format:

- bi-directional 
- full-duplex 
- in real-time.

The server can send data to the client at any time. Because it runs over TCP, it also provides a low-latency low-level communication and 
reduces the overhead of each message. Messages over websockets are sent in frames, these frames have only 2 byte overhead. Messages over websockets are sent in frames, these frames have only 2 byte overhead. 

## 2. JSR 356
JSR 356 or the Java API for WebSocket, specifies an API that Java developers can use for integrating WebSockets withing their applications – both on the server side as well as on the Java client side.

This Java API provides both server and client side components:

- Server: everything in the javax.websocket.server package.
- Client: the content of javax.websocket package, which consists of client side APIs and also common libraries to both server and client.
## 3. Endpoint Configuration
There are two ways of configuring endpoints: annotation-based and extension-based. You can either extend the javax.websocket.Endpoint class or use dedicated method-level annotations. As the annotation model leads to cleaner code as compared to the programmatic model, the annotation has become the conventional choice of coding. In this case, WebSocket endpoint lifecycle events are handled by the following annotations:

- @ServerEndpoint: If decorated with @ServerEndpoint, the container ensures availability of the class as a WebSocket server listening to a specific URI space
- @ClientEndpoint: A class decorated with this annotation is treated as a WebSocket client
- @OnOpen: A Java method with @OnOpen is invoked by the container when a new WebSocket connection is initiated
- @OnMessage: A Java method, annotated with @OnMessage, receives the information from the WebSocket container when a message is sent to the endpoint
- @OnError: A method with @OnError is invoked when there is a problem with the communication
- @OnClose: Used to decorate a Java method that is called by the container when the WebSocket connection closes
