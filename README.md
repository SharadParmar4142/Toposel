# User Management System

A simple user management system built with Express.js and MongoDB. It allows users to register, login, and search for user information. JWT tokens are used for authentication.

## Features

- User Registration
- User Login
- Search User by Username or Email
- JWT Authentication

## Tech Stack

- Node.js
- Express.js
- MongoDB
- JWT

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
2. Install dependencies:
    npm install
3. Create a .env file in the root directory and add the following environment variables:
    CONNECTION_STRING=your_mongodb_connection_string
    ACCESS_TOKEN_SECRET=your_secret_key
    PORT=3200
4. Start the server:
    npm start


API Endpoints
1. User Registration
Endpoint: POST /user/register
Request Body:

{
  "username": "testuser",
  "password": "password123",
  "fullName": "Test User",
  "gender": "Male",
  "dateOfBirth": "1990-01-01",
  "country": "USA",
  "email": "testuser@example.com"
}

2. User Login
Endpoint: POST /user/login
Request Body:

{
  "email": "testuser@example.com",
  "password": "password123"
}


3. Search User
Endpoint: GET /user/search?username=testuser
Headers
{
  "Authorization": "Bearer <your_jwt_token>"
}
