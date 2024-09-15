# Real-Time Collaborative Code Editor

A **Real-Time Collaborative Code Editor** that allows multiple users to work on the same code simultaneously, offering real-time collaboration features with the support of Redis for session management, Socket.IO for real-time communication, React for the frontend, Node.js for the backend, and CodeMirror as the code editor.

## Features

- **Real-Time Synchronization**: Collaborative coding with real-time updates across all users.
- **CodeMirror Integration**: CodeMirror provides syntax highlighting and an efficient, extensible code editing experience.
- **Redis-Powered Session Management**: Redis ensures scalability and reliable management of multiple user sessions.
- **User Authentication**: Allows users to join and leave coding sessions seamlessly.
- **Language Support**: CodeMirror offers syntax support for various programming languages.
- **Conflict Resolution**: Prevents issues during simultaneous edits through efficient synchronization mechanisms.

## Tech Stack

- **Frontend**:
  - React.js
  - CodeMirror (for code editing interface)
  - Socket.IO (for WebSocket communication)
  
- **Backend**:
  - Node.js with Express.js (server)
  - Socket.IO (for real-time updates)
  - Redis (for session management and persistence)

- **Database**:
  - Redis (to store session states and manage real-time collaborative edits)

## Prerequisites

To run this project locally, ensure you have the following installed:

- Node.js (v14.x or higher)
- npm (v6.x or higher)
- Redis server

## Setup and Installation

### Steps to Run Locally

1. **Install dependencies**:
   ```bash
   npm i
   ```

2. **Set up Redis**:
   Ensure Redis is installed and running on your system. You can start Redis with:
   ```bash
   redis-server
   ```

3. **Configure Environment Variables**:
   Create a `.env` file in the root directory with the following variables:
   ```bash
   PORT=4000
   REDIS_URL=redis://localhost:6379
   ```

4. **Run the Server**:
   Go back to the project root directory and start the server:
   ```bash
   npm run dev
   ```

5. **Access the Application**:
   Open your browser and go to `http://localhost:3000` to start using the real-time collaborative editor.

### Project Structure

- **src/**: Contains the React frontend with the CodeMirror editor.
- **server/**: Contains the Node.js backend with Socket.IO and Redis for real-time collaboration and session management.

### Frontend (React)

- `src/components/RealTimeEditor.jsx`: Implements the collaborative code editor using CodeMirror and Socket.IO.
- `src/App.jsx`: Manages routing and the main application structure.

### Backend (Node.js)

- `server.js`: The main entry point for the Node.js server, setting up WebSocket connections via Socket.IO.

## Usage

1. **Create or Join a Session**: When you access the application, you can create a new collaborative session or join an existing one.
2. **Start Editing**: CodeMirror enables syntax-highlighted code editing. Any changes made by one user will be reflected in real-time for all users in the same session.
3. **Redis for Persistence**: Sessions are managed via Redis to ensure smooth, scalable performance across multiple users.

## Deployment

To deploy the application on a service like Heroku or AWS:

1. **Set up Redis**: Ensure your platform supports Redis or use a managed Redis service like RedisLabs.
2. **Configure environment variables** for Redis and set the `REDIS_URL`.
3. **Deploy**: Push your code to your desired platform, ensuring proper setup for Node.js, React, and Redis.

## Contributing

Contributions are welcome! Here’s how you can contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m "Add new feature"`).
4. Push the branch (`git push origin feature-branch`).
5. Open a pull request to merge your changes into `main`.
