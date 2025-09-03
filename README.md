**Real-Time Chat Application (Socket.IO)**
This project is a real-time chat application built using Socket.IO
It enables instant, bidirectional communication between the client and the server, making it possible for users to send and receive messages seamlessly without page reloads.
The app demonstrates the core functionality of Socket.IO as outlined in its official documentation:
 **Features**
Real-time messaging – users can send and receive chat messages instantly.
Event-driven communication – messages are sent through custom events (chat message) between client and server.
Broadcasting – messages can be broadcasted to all connected clients.
Automatic reconnection – if a client loses connection, Socket.IO automatically tries to reconnect.
Transport fallback – supports WebSockets primarily, but falls back to HTTP long-polling when necessary.
Message reliability – supports acknowledgements and delivery guarantees (at most once, at least once, exactly once).

**How It Works**
The server is built with Node.js and Express, serving both the static HTML page and handling socket connections.
The client (a simple HTML page) connects using the Socket.IO client library.
When a user submits a message:
The client emits a "chat message" event.
The server listens for the event and broadcasts it to all connected clients.
All clients update in real time without refreshing.
