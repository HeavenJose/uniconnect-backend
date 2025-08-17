UniConnect - Back-End ⚙️
This repository contains the Node.js, Express, and MongoDB backend for the UniConnect application, a comprehensive digital platform for university students. This server provides a robust RESTful API to handle all data management, user authentication, and business logic for the platform.

⬅️ Link to the Front-End Repository: uniconnect-frontend

🚀 Core Functionality
This backend is designed to support a feature-rich social and academic hub. It manages the data and logic for:

Secure User Authentication: Handles user registration and login using password hashing (bcrypt) and secure session management with JSON Web Tokens (JWT).

Data Management: Provides full CRUD (Create, Read, Update, Delete) operations for all of the application's main features.

Relational Data: Manages the relationships between users and their created content (notes, projects, listings, etc.).

Private Messaging: Includes a system for creating and managing private conversations between users related to marketplace listings.

🛠️ Tech Stack
Runtime Environment: Node.js

Framework: Express.js

Database: MongoDB with Mongoose ODM

Authentication: JSON Web Tokens (JWT), bcrypt.js

Middleware: CORS

API Endpoints
The server exposes the following RESTful API endpoints. All private routes require a valid JWT to be sent in the x-auth-token header.

Method

Endpoint

Description

Access

Users







POST

/api/users/register

Registers a new user.

Public

POST

/api/users/login

Authenticates a user and returns a JWT.

Public

GET

/api/users/me

Gets the profile of the currently logged-in user.

Private

Notes







POST

/api/notes

Creates a new note for the logged-in user.

Private

GET

/api/notes

Fetches all notes.

Private

Projects







POST

/api/projects

Creates a new project for the logged-in user.

Private

GET

/api/projects

Fetches all projects.

Private

Events







POST

/api/events

Creates a new event.

Private

GET

/api/events

Fetches all events.

Private

Listings







POST

/api/listings

Creates a new marketplace listing.

Private

GET

/api/listings

Fetches all listings.

Private

Conversations







POST

/api/conversations

Sends a message in a conversation.

Private

GET

/api/conversations/listing/:id

Gets the conversation for a specific listing.

Private

GET

/api/conversations/notifications

Gets unread message notifications.

Private

PUT

/api/conversations/read/:id

Marks a conversation as read.

Private

⚙️ Setup and Installation
To get a local copy of the backend up and running, follow these steps.

Prerequisites
Node.js and npm installed

A MongoDB Atlas account and connection string

Installation
Clone the repository:

git clone https://github.com/HeavenJose/uniconnect-backend.git

Navigate into the project directory:

cd uniconnect-backend

Install the necessary dependencies:

npm install

Create a .env file in the root of the project and add your environment variables:

MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_jwt_key

Start the server:

node server.js

The server will start on http://localhost:5000.
