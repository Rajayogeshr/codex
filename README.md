# Project Overview

Codex is a powerful tool designed to streamline your workflow and enhance productivity. This project aims to provide a reliable and efficient platform for managing your coding tasks and resources.

# Features
- **User Authentication**: Secure login and user management.
- **Task Management**: Create, update, and delete coding tasks.
- **Collaboration Tools**: Share tasks and collaborate with team members.
- **Real-time Notifications**: Get timely alerts and updates.

# Technology Stack
- **Frontend**: React, Redux
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Styles**: Tailwind CSS

# Setup Instructions
## Prerequisites
- Node.js (version 14 or higher)
- MongoDB (local or cloud)

## Installation Steps
1. Clone the repository:
   
   ```bash
   git clone https://github.com/Rajayogeshr/codex.git
   cd codex
   ```

2. Install dependencies:
   
   ```bash
   npm install
   ```

3. Configure the database connection in the `.env` file.

4. Start the application:
   
   ```bash
   npm start
   ```

# API Endpoints
## Authentication
- **POST** `/api/auth/login` - Login users
- **POST** `/api/auth/register` - Register new users

## Tasks
- **GET** `/api/tasks` - Get all tasks
- **POST** `/api/tasks` - Create a new task
- **PUT** `/api/tasks/:id` - Update a task
- **DELETE** `/api/tasks/:id` - Delete a task

# Database Schema
## Users
- **_id**: ObjectId
- **username**: String
- **password**: String
- **email**: String

## Tasks
- **_id**: ObjectId
- **title**: String
- **description**: String
- **status**: String ('pending' | 'completed')
- **createdBy**: ObjectId (reference to User)

# Usage Examples
## Creating a Task
```bash
curl -X POST -H "Content-Type: application/json" \
  -d '{"title":"My New Task","description":"Details about the task"}' \
  http://localhost:5000/api/tasks
```

# Deployment Guide
To deploy this application:
1. Build the frontend with `npm run build`.
2. Deploy the compiled code to a server.
3. Set up environment variables for production.
4. Make sure the server is running the Node.js application and the database is accessible.

# License
This project is licensed under the MIT License. See the LICENSE file for details.