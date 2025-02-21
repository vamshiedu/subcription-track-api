
# Subscription Tracker API

A **Node.js API** for managing user subscriptions, allowing users to **sign up, sign in, create subscriptions**, and receive **reminders** for upcoming renewals.

## Features

### 1. **User Authentication**
- **Sign up**
- **Sign in**
- **Sign out**

### 2. **Subscription Management**
- **Create subscriptions**
- **Get user subscriptions**
- **Send reminders** for upcoming renewals

### 3. **Middleware**
- **Arcjet Middleware** for security
- **Error handling** middleware

---

## Getting Started

### Prerequisites
Ensure the following are installed on your system:
- **Node.js**
- **npm** (Node Package Manager)
- **MongoDB**

### Installation Steps

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/vamshiedu/subscription-tracker-api.git
   ```

2. **Navigate into the Project Directory:**

   ```bash
   cd subscription-tracker-api
   ```

3. **Install the Dependencies:**

   ```bash
   npm install
   ```

4. **Set up Environment Variables:**
   Create a `.env` file in the root directory and include the following:

   ```bash
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

5. **Start the Application:**

   ```bash
   npm run dev
   ```

The API will now be running on `http://localhost:5500`.

---

## API Endpoints

### **Authentication Routes**

- `POST /api/v1/auth/sign-up` - Sign up a new user
- `POST /api/v1/auth/sign-in` - Sign in an existing user
- `POST /api/v1/auth/sign-out` - Sign out the current user

### **User Management Routes**

- `GET /api/v1/users` - Get all users
- `GET /api/v1/users/:id` - Get a specific user by ID

### **Subscription Management Routes**

- `POST /api/v1/subscriptions` - Create a new subscription
- `GET /api/v1/subscriptions/user/:id` - Get all subscriptions for a specific user

### **Workflow Routes**

- `POST /api/v1/workflows/subscription/reminder` - Send reminders for subscription renewals

---

## Technologies Used

- **Backend**: Node.js, Express
- **Database**: MongoDB, Mongoose
- **Authentication**: JWT (JSON Web Tokens)
- **Email**: Nodemailer
- **Security**: Arcjet
- **Task Scheduling**: Upstash Workflow

---

## Contribution

Feel free to contribute to this project by creating **issues** or submitting **pull requests**.
