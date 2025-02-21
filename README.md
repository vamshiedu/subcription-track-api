# Subscription Tracker API

This is a Node.js API for managing user subscriptions. It allows users to sign up, sign in, create subscriptions, and receive reminders for upcoming renewals.

## Features

- **User Authentication**:
  - Sign up
  - Sign in
  - Sign out

- **Subscription Management**:
  - Create subscriptions
  - Get user subscriptions
  - Send reminders for upcoming renewals

- **Middleware**:
  - Arcjet middleware for security
  - Error handling middleware

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Node.js
- npm (Node Package Manager)
- MongoDB

### Installation

1. Clone the repository:

   ```cmd
   git clone https://github.com/vamshiedu/subscription-tracker-api.git

2. Navigate into the project directory:
    ```cmd
    cd subscription-tracker-api
  
3. Install dependencies:
    ```cmd
    npm install

### Environment Variables

4. Create a `.env` file in the root directory and add the following environment variables:

    ```env
    PORT=5500
    SERVER_URL="http://localhost:5500"
    NODE_ENV=development
    DB_URI=<your_mongodb_uri>
    JWT_SECRET=<your_jwt_secret>
    JWT_EXPIRES_IN=1d
    ARCJET_KEY=<your_arcjet_key>
    ARCJET_ENV="development"
    QSTASH_URL=<your_qstash_url>
    QSTASH_TOKEN=<your_qstash_token>
    EMAIL_PASSWORD=<your_email_password>
    ```

5. Start the application:

    ```cmd
    npm run dev
    ```

The API will run on http://localhost:5500.

6. API Endpoints
    ```cmd
  Auth
    POST /api/v1/auth/sign-up - Sign up a new user
    POST /api/v1/auth/sign-in - Sign in an existing user
    POST /api/v1/auth/sign-out - Sign out the current user
    Users
    GET /api/v1/users - Get all users
    GET /api/v1/users/:id - Get a specific user
  Subscriptions
    POST /api/v1/subscriptions - Create a new subscription
    GET /api/v1/subscriptions/user/:id - Get subscriptions for a specific user
  Workflows
    POST /api/v1/workflows/subscription/reminder - Send reminders for subscription renewals
    ```
7. Technologies Used
```cmd
  Backend: Node.js, Express
  Database: MongoDB, Mongoose
  Authentication: JWT
  Email: Nodemailer
  Security: Arcjet
  Task Scheduling: Upstash Workflow
  Contributing
  Feel free to contribute to this project by creating issues or submitting pull requests.
  ```