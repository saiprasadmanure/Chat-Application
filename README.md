# Real-time Chat App
COMPANY: CODTECH IT SOLUTIONS 
NAME : M SAIPRASAD 
INTERN ID:CT06DL980 
DOMAIN: FULL STACK WEB DEVELOPMENT
DURATION : 6 WEEKS 
MENTOR : NEELA SANTOSH

This is a simple real-time chat application built using Node.js, Express, and Socket.IO.

## How to Run

1. Install dependencies:
```
npm install
```

2. Start the server:
```
npm start
```

3. Open your browser and go to:
```
http://localhost:3000
```

Start chatting in real-time!

📘 Project Description: Real-Time Chat Application using Socket.IO
This project is a simple, yet powerful real-time chat application built using Node.js, Express.js, and Socket.IO. The goal of this application is to enable multiple users to communicate with each other in real time, with messages appearing instantly across all clients without needing to reload the page. This solution demonstrates key concepts of real-time bi-directional communication between the server and the clients, a common requirement in modern web applications such as WhatsApp, Messenger, or collaborative tools like Slack.

🛠 Technologies Used
Node.js: A JavaScript runtime environment used to run the backend of the application. It allows us to create a web server that listens for incoming HTTP requests and manages WebSocket communication.

Express.js: A lightweight web application framework for Node.js. It simplifies the server setup, manages routing, and serves static files like HTML, CSS, and JavaScript.

Socket.IO: A JavaScript library that enables real-time, event-based communication between clients and a server. It uses WebSockets under the hood and falls back to other protocols when needed, ensuring compatibility and performance.

HTML/CSS/JavaScript: Used for building the frontend user interface. HTML provides the structure, CSS handles the styling, and JavaScript (via client.js) communicates with the server using Socket.IO.

🔧 How the Application Works
The project is organized into two main parts: the server-side and the client-side.

1. Backend (server.js)
The server file starts by importing the necessary libraries: express, http, and socket.io. An Express app is created, and the HTTP server is passed to the socket.io instance. The app serves the static files from the public/ directory, which contains all the frontend code.

When a user connects to the server, the io.on('connection') event is triggered. This means the server has established a WebSocket connection with a client. Inside this block, the server listens for a custom event chat message. When this event is received (i.e., when a user sends a message), the server broadcasts that message to all connected clients, ensuring that everyone sees the message in real time.

The server also logs when a user connects or disconnects, which can be useful for debugging or extending the app later with more features like "user joined" or "user left" notifications.

2. Frontend
index.html: This is the main webpage that users interact with. It contains a chat interface with a message list (<ul id="messages">) and an input form where users can type and send messages.

style.css: This file styles the chat interface. It ensures the chat box looks clean and readable, with some modern UI elements like shadows and padding. The layout is responsive enough to work on basic screen sizes.

client.js: This is the brain of the frontend. When the page loads, it establishes a Socket.IO connection to the server using const socket = io();. It then listens for the form submission. When a message is submitted, it emits the chat message event to the server. It also listens for incoming chat message events and updates the UI accordingly by appending new list items (<li>) to the messages container.

🧩 Features
Real-time messaging with no page reload

Lightweight and fast

Clean user interface

Easy to deploy locally or on platforms like Render, Replit, or Glitch

Scalable for adding new features like usernames, message timestamps, or rooms

🚀 How to Run
To run the application:

Place all files in a folder named chat-app.

Run npm install to install dependencies.

Run npm start to launch the server.

Open your browser at http://localhost:3000.

Open multiple tabs or devices to test real-time chat.

📝 Conclusion
This chat application is a foundational real-time web project that demonstrates the use of Socket.IO for instant communication, which is a core requirement in many modern apps. It provides hands-on experience with event-driven architecture, server-client communication, and basic frontend/backend integration. With minimal setup, it's also a great base to build more advanced chat features like private messaging, typing indicators, or persistent chat rooms.

Let me know if you'd like me to add user authentication, message timestamps, or deploy this app live.
