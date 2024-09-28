# Chatterly

ChatApp is a real-time chat application built using **Node.js** and **Express.js**, with WebSockets for real-time messaging. Users can create chat rooms, send messages, and interact with others in a secure environment.

## Features

- **Real-time Messaging:** Chat with others in real-time using WebSocket technology.
- **Rooms:** Create and join specific chat rooms for focused discussions.
- **User Authentication:** Secure login and registration system.
- **Responsive UI:** Works seamlessly on desktop and mobile devices.
- **Typing Indicators:** See when someone is typing in real-time.
- **Message History:** Access chat history upon joining a room.
- **Emoji Support:** Express yourself with emojis in your conversations.
- **Private Messaging:** Send direct messages to specific users.

## Tech Stack

- **Node.js** - Backend runtime environment.
- **Express.js** - Framework for handling routing and server logic.
- **Socket.IO** - For real-time, bidirectional event-based communication.
- **MongoDB** - Database to store user data, chat rooms, and message history.
- **JWT (JSON Web Tokens)** - For secure user authentication and session management.
- **Bootstrap / CSS** - For responsive front-end design.

## Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/) (for database)
- [Git](https://git-scm.com/)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/chat-app.git
   cd chat-app
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables by creating a `.env` file in the project root and add the following:

   ```
   PORT=3000
   MONGO_URI=mongodb://localhost:27017/chatapp
   JWT_SECRET=your_secret_key
   ```

4. Start the MongoDB service:

   ```bash
   mongod
   ```

5. Start the application:

   ```bash
   npm start
   ```

   The app will run at `http://localhost:3000`.

### Project Structure

```bash
chat-app/
│
├── public/               # Static assets (CSS, images, JS)
├── views/                # Frontend templates (EJS, Pug, etc.)
├── routes/               # Express route handlers
├── models/               # Mongoose models for User, ChatRoom, Message
├── controllers/          # Business logic for routes
├── middleware/           # Authentication, error handling middleware
├── socket/               # Socket.IO event handling
├── .env                  # Environment variables
├── app.js                # Main application file
├── package.json          # Project metadata and dependencies
└── README.md             # Project documentation
```

### Endpoints

- **GET /** - Home page for the chat app.
- **POST /login** - User login.
- **POST /register** - User registration.
- **GET /chat/:room** - Join or create a chat room.

### WebSocket Events

- **connection** - When a user connects to the chat.
- **disconnect** - When a user disconnects.
- **message** - Send a message in the chat room.
- **typing** - Broadcast typing status to other users.

## Contributing

1. Fork the project.
2. Create your feature branch: `git checkout -b feature/YourFeature`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature/YourFeature`.
5. Open a pull request.
