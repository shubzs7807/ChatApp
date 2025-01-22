# Real-Time Chat Application

This is a real-time chat application where users can sign up, log in, view a list of all registered users, and chat with them. The chat messages are sent and received in real-time using WebSocket, and all user data and chat messages are stored in MongoDB.

## Features:
- **Sign Up and Login**: Users can sign up and log in.
- **Collapsible Left Menu**: Displays all registered users.
- **Initiate Chat**: The logged-in user can select any user from the left menu and start a conversation.
- **Real-Time Messaging**: WebSocket is used to send and receive messages in real-time.
- **Old Messages**: Chat history is retrieved and displayed on chat initiation.
- **User Interface**: A user-friendly chat interface is provided for seamless interaction.

## Technologies Used:
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Node.js, Express, WebSocket
- **Database**: MongoDB
- **Real-Time Communication**: WebSocket (using `ws` library)

## Installation & Running the Project:

### Prerequisites:
- **Node.js** installed on your machine. You can download it from [nodejs.org](https://nodejs.org/).
- **MongoDB** installed or use a cloud-based database service like MongoDB Atlas.

### Steps to Run the Application:

1. **Clone the repository**:
  
   git clone https://github.com/your-username/chat-app.git


Navigate to the project directory:

cd chat-app

Install dependencies: Install both frontend and backend dependencies by running:

npm install

Set up MongoDB:

If you are using a local MongoDB instance, make sure it is running.
Alternatively, you can set up a MongoDB Atlas account and replace the MongoDB URI in the server.js file.
Start the backend server: Run the following command to start the Node.js server:

node server.js
Open the application: Open index.html in your browser to interact with the chat application.

File Structure:

index.html: Main chat interface and structure.
styles.css: Styling for the chat UI.
app.js: Frontend JavaScript to handle UI and WebSocket communication.

Backend:

server.js: Node.js server that handles API requests and WebSocket communication.
models/user.js: MongoDB model for storing user data.
models/message.js: MongoDB model for storing chat messages.
routes/userRoutes.js: API routes for user authentication and chat history.

How the Application Works:

User Authentication:

Users can sign up and log in. The application uses sessions or JWT for maintaining login state.
All registered users are displayed in a collapsible menu on the left side.

Starting a Chat:

The logged-in user can select any user from the list to initiate a chat.
The chat history (if any) is retrieved from the database.
Real-Time Messaging:

WebSocket is used to facilitate real-time messaging. When a user sends a message, the other user(s) receive it instantly.
Storing and Retrieving Messages:

All messages are stored in MongoDB, and old messages are displayed when the chat is initiated.

API Endpoints:
POST /signup:

Sign up a new user. Requires username and password.
POST /login:

Log in an existing user. Requires username and password.
GET /users:

Get all registered users. Available only when the user is logged in.
GET /messages/:userId:

Get the chat history with a specific user.
